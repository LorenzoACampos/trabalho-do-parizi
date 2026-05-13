# **Requisitos Funcionais e Não Funcionais**

---

# **Requisitos Funcionais**

## **RF01 — Alerta automático de ausências consecutivas enviado ao coordenador**

### **Critério de aceitação**
Toda vez que um professor registrar a **2ª falta consecutiva** de um aluno em uma disciplina, o sistema gera automaticamente uma notificação ao coordenador.

A notificação contém:
- **nome do aluno**
- **disciplina**
- **link direto ao perfil**

Nenhuma falta consecutiva pode deixar de gerar alerta — taxa de falsos negativos deve ser **zero**, verificável por auditoria de logs.

### **Medidas**
- **0 falsos negativos** nos logs de alerta.
- Notificação contém os **3 campos obrigatórios**:
  - nome
  - disciplina
  - link

---

## **RF02 — Upload de diário de frequência pelo professor com validação de formato**

### **Critério de aceitação**
O sistema aceita arquivos **`.xlsx`** ou **`.csv`** no modelo padronizado pela instituição.

Arquivos com:
- colunas faltando
- matrícula inválida
- datas fora do semestre vigente

devem ser rejeitados com mensagem de erro descritiva identificando:
- **linha**
- **campo com problema**

O professor consegue corrigir e reenviar sem acionar suporte técnico.

### **Medidas**
- Mensagem de erro aponta **linha e campo específico**.
- **0 arquivos inválidos** aceitos silenciosamente.

---

## **RF03 — Dashboard de frequência por aluno com filtros (visão coordenador)**

### **Critério de aceitação**
O coordenador visualiza em uma única tela **todos os alunos do curso** com o percentual de presença por disciplina no semestre vigente.

### **Filtros disponíveis**
- **turma**
- **disciplina**
- **faixa de frequência** (ex.: abaixo de 75%)

Todos os filtros funcionam de forma combinada.

Nenhum aluno matriculado pode ficar fora da listagem.

### **Medidas**
- **100% dos alunos matriculados listados**.
- Filtros combinados funcionam sem erro em **100% dos testes**.

---

## **RF04 — Relatório exportável de alunos em risco por turma**

### **Critério de aceitação**
O coordenador gera com um clique um relatório em:
- **PDF**
- **`.xlsx`**

O relatório contém:
- **nome**
- **matrícula**
- disciplinas com frequência abaixo do limiar
- número de faltas consecutivas atuais

O limiar é configurável entre **50% e 90%**.

### **Restrições**
O relatório **não pode conter**:
- CPF
- endereço
- dados financeiros

### **Medidas**
- Limiar configurável entre **50% e 90%**.
- **0 campos sensíveis** presentes no relatório.

---

## **RF05 — Visão de frequência do aluno restrita à disciplina do professor**

### **Critério de aceitação**
O professor visualiza apenas:
- percentual de presença dos alunos
- dentro da sua própria disciplina

Nenhum dado de outras disciplinas pode ser acessado:
- percentual global
- datas de faltas em outras matérias
- nomes de outros professores

Verificação feita por:
- inspeção de interface
- teste de perfil `"professor"`

### **Medidas**
- **0 campos de outras disciplinas** visíveis para professores.

---

## **RF06 — Indicador de flexibilidade de oferta por disciplina (visão coordenador)**

### **Critério de aceitação**
O sistema exibe ao coordenador disciplinas com maior índice combinado de:
- faltas
- relatos de dificuldade de conciliação com trabalho

O cruzamento utiliza obrigatoriamente:
- dados de frequência (**RF02**)
- relatos dos alunos

### **Objetivo**
Identificar disciplinas candidatas a:
- oferta híbrida
- aulas gravadas

O cruzamento deve ser exibido de forma:
- **agregada**
- **sem identificação individual**

### **Motivação**
- **59%** apontaram conciliação trabalho/curso como principal obstáculo.
- **18%** indicaram flexibilidade de horário como suporte de maior impacto.

### **Medidas**
- **0 identificações individuais** exibidas ao coordenador.
- Cruzamento considera obrigatoriamente as **duas fontes de dados**.

---

## **RF07 — Painel de oportunidades de estágio e emprego acessível ao aluno**

### **Critério de aceitação**
O sistema exibe oportunidades cadastradas pela:
- coordenação
- parceiros institucionais

### **Filtros disponíveis**
- área
- modalidade (**presencial/remoto**)
- carga horária

### **Campos obrigatórios da vaga**
- nome da empresa
- descrição da vaga
- requisitos
- forma de candidatura

### **Motivação**
- **76%** dos respondentes apontaram parcerias com empresas como principal fator de permanência no curso.

### **Medidas**
- **100% das oportunidades** exibem os 4 campos obrigatórios.
- Filtros funcionam de forma combinada.

---

## **RF08 — Configuração de limiares de alerta pelo coordenador com log de auditoria**

### **Critério de aceitação**
O coordenador define:
- número de faltas consecutivas
- percentual mínimo de presença

### **Valores padrão**
- faltas consecutivas: **2**
- frequência mínima: **75%**

Toda alteração gera log contendo:
- data
- hora
- usuário responsável

O log:
- **não pode ser editado**
- **não pode ser excluído**

### **Medidas**
- Log gerado em **100% das alterações**.
- **0 operações** de edição ou exclusão permitidas.

---

## **RF09 — Notificação automática de frequência baixa diretamente ao aluno**

### **Critério de aceitação**
O sistema envia notificações automáticas em dois momentos:

### **Alerta Preventivo**
Quando a frequência cair abaixo de **85%**.

Mensagem:
- alerta de aproximação do limite mínimo (**75%**)

### **Alerta Crítico**
Quando a frequência cair abaixo de **75%**.

Mensagem:
- risco de reprovação por falta

Em ambos os casos:
- o coordenador também é notificado
- os limiares são configuráveis via **RF08**

### **Medidas**
- **0 casos sem notificação** ao cruzar os limiares.
- Conteúdo preventivo e crítico são distintos.
- **100% dos alertas críticos** notificam simultaneamente o coordenador.

---

## **RF10 — Autodeclaração voluntária e anônima de obstáculo pelo aluno com sinalização vocacional**

### **Critério de aceitação**
Uma vez por semestre, o aluno recebe convite opcional para indicar seu principal obstáculo:

- tempo/trabalho
- financeiro
- pedagógico
- vocacional

A resposta é:
- **anônima por padrão**

O coordenador acessa apenas:
- dados agregados por turma

O dado individual só é vinculado ao aluno quando ele marcar explicitamente:

> **"quero ser contactado pela coordenação"**

### **Ação automática**
Quando o aluno selecionar `"vocacional"`:
- o sistema exibe automaticamente canais de orientação profissional

### **Notificação ao coordenador**
O coordenador recebe alerta agregado quando:
- mais de **10% da turma** selecionar `"vocacional"`

Sem identificação individual.

### **Motivação**
- **12%** das respostas do questionário foram de natureza vocacional.

### **Medidas**
- **0 identificações individuais** sem opt-in.
- Opt-in:
  - explícito
  - separado
  - não pré-marcado
- Mensagem vocacional exibida em **100% dos casos**.
- Coordenador notificado apenas acima de **10%**.

---

# **Requisitos Não Funcionais**

## **RNF1 — Privacidade e controle de acesso por perfil (LGPD)**

O sistema deve implementar **3 perfis distintos**:

### **Coordenador**
Acesso a:
- frequência
- histórico de intervenções
- agregados dos questionários
- perfis de contato

### **Professor**
Acesso apenas:
- à frequência dos alunos de sua própria disciplina

### **Aluno**
Acesso apenas:
- aos próprios dados
- ao painel de oportunidades

### **Regras adicionais**
- Dados do **RF06** e **RF10** devem ser armazenados separadamente dos dados acadêmicos.
- Coordenador acessa apenas dados agregados.
- Dados individuais exigem consentimento explícito.

Toda tentativa de acesso indevido:
- deve ser bloqueada
- deve gerar log de auditoria

### **Verificações**
- Professor não acessa frequência de outra disciplina.
- Coordenador não acessa dados individuais sem opt-in.
- Toda tentativa indevida gera log.

---

## **RNF2 — Disponibilidade nos períodos críticos do calendário acadêmico**

O sistema deve garantir disponibilidade mínima de **99,5%** nas últimas 4 semanas de cada semestre.

### **Requisitos adicionais**
- Uploads processados por **fila assíncrona**.
- Falhas não descartam arquivos válidos.
- Sistema exibe mensagem clara em indisponibilidade.
- Dados enviados antes da falha permanecem íntegros.

### **Verificações**
- Disponibilidade ≥ **99,5%**.
- **0 arquivos válidos descartados**.
- Integridade validada após recuperação.

---

## **RNF3 — Anonimização e separação de dados sensíveis por origem**

Os dados devem ser armazenados separadamente conforme a origem:

| **Origem** | **Tipo de dado** |
|---|---|
| **RF02** | Frequência acadêmica |
| **RF10** | Autodeclaração de obstáculos |
| **RF06** | Relatos de conciliação |

### **Regras**
- Nenhum relatório pode cruzar automaticamente dados sensíveis com identificação individual.
- Cruzamento individual só ocorre com consentimento registrado.
- O isolamento deve ser garantido pela arquitetura do sistema.

### **Verificações**
- Tabelas separadas no banco de dados.
- Nenhuma query retorna dados individuais sem consentimento.
- Coordenador não consegue cruzar dados individualmente sem opt-in.
