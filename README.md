## Trabalho da plataforma SaveStudent

#  Resultados da Entrevista com a Coordenação
<details>
  <summary><b>1. Experiência Prática e Casos de Risco</b></summary>

  **Pergunta:** Me diga um caso recente que você percebeu um risco de evasão em um aluno. O que levou a pensar nisso e como fez para tentar resolver?
  
  **Objetivo:** Entender o gatilho emocional e comportamental que não está nos dados frios.

  **Resposta:** O sinal mais claro é a **ausência em avaliações**. O processo atual é informal: tenta-se contato por mensagem ou conversas entre professores para checar se o aluno parou de frequentar as outras disciplinas também.
</details>

<details>
  <summary><b>2. Sinais de Alerta (Faro do Coordenador)</b></summary>

  **Pergunta:** Na sua experiência, quais são os principais sinais de que um aluno vai evadir? Aqueles que quando você "bate o olho" já sabe?
  
  **Objetivo:** Validar quais indicadores (faltas, notas, comportamento) devem ter maior peso nos alertas do sistema.

  **Resposta:** O principal indicador são **duas semanas consecutivas de falta**. Em disciplinas de um encontro semanal, isso significa 15 dias longe da aula, o que representa um risco crítico de desconexão com o curso.
</details>

<details>
  <summary><b>3. Processo de Intervenção Atual</b></summary>

  **Pergunta:** Hoje, ao identificar um risco, qual é o processo de intervenção? Com quem se fala? É feito algum registro?
  
  **Objetivo:** Mapear o fluxo de trabalho atual para que o sistema possa automatizar ou facilitar essas etapas.

  **Resposta:** Não há registro oficial. A intervenção baseia-se em conversas entre docentes para entender se a desistência é em apenas uma matéria (comum na graduação) ou se é um abandono total do curso.
</details>

<details>
  <summary><b>4. Funcionalidade Essencial (Dashboard Diário)</b></summary>

  **Pergunta:** Se existisse uma plataforma, qual seria a funcionalidade que você abriria toda manhã? Qual informação não pode faltar?
  
  **Objetivo:** Definir o "MVP" (Mínimo Produto Viável) e a tela principal do Coordenador.

  **Resposta:** Um **alerta automático por e-mail** baseado no "número mágico" de 2 semanas de falta. É necessário um **dashboard centralizado**, pois hoje os dados no SIGA são dispersos e difíceis de visualizar de forma estruturada.
</details>

<details>
  <summary><b>5. Riscos e Atualização de Dados</b></summary>

  **Pergunta:** O que te preocupa em ter tantos dados reunidos? O que poderia dar errado?
  
  **Objetivo:** Identificar gargalos técnicos e operacionais que podem invalidar a utilidade da ferramenta.

  **Resposta:** A **taxa de atualização**. Como não há acesso via API ao SIGA, o risco é o dado ficar defasado. O ideal seria que os professores subissem os diários de classe semanalmente para garantir dados reais.
</details>

<details>
  <summary><b>6. Segurança e Privacidade (LGPD)</b></summary>

  **Pergunta:** Quais deveriam ser as principais medidas de segurança e privacidade da plataforma?
  
  **Objetivo:** Levantar Requisitos Não Funcionais (RNFs) focados em proteção de dados e permissões de perfil.

  **Resposta:** Restrição de visibilidade. Um professor **não deve ver detalhes** de ausências em outras disciplinas. O acesso detalhado deve ser restrito ao professor da matéria e ao coordenador (este com visão geral).
</details>

<details>
  <summary><b>7. Agilidade e Relatórios</b></summary>

  **Pergunta:** Se eu te pedisse um relatório completo da situação de risco agora, quanto tempo levaria e o que isso exigiria de você?
  
  **Objetivo:** Medir o ganho de produtividade que a plataforma trará em comparação ao processo manual atual.

  **Resposta:** Levaria muito tempo e trabalho manual. Seria necessário baixar dezenas de PDFs, cruzar listas de alunos manualmente e montar uma matriz do zero. Hoje, as informações não estão consolidadas.
</details>

---
*Dados coletados para fundamentar a elaboração dos Requisitos Funcionais e de Interface do projeto.*
# Perguntas do Questionário

<details>
  <summary><b>1. Expectativas Profissionais</b></summary>

  **Em uma escala de 1 a 5, o quanto o currículo atual do curso (disciplinas e conteúdos) atende às suas expectativas profissionais?**

  - **(1)** Não atende nada - O que estudo parece irrelevante para o mercado.
  - **(2)** Atende pouco - Muita teoria e pouca prática tecnológica.
  - **(3)** Neutro - Atende em partes, mas falta atualização.
  - **(4)** Atende bem - Vejo conexão entre as aulas e a carreira de TI.
  - **(5)** Atende totalmente - O curso me prepara exatamente para o que o mercado exige.
</details>

<details>
  <summary><b>2. Maiores Obstáculos</b></summary>

  **Qual destes fatores representa hoje o maior obstáculo para a continuidade dos seus estudos?**

  - **Financeiro:** Dificuldade em pagar, transporte ou infraestrutura (computador/internet).
  - **Pedagógico:** Grande dificuldade em disciplinas específicas (Ex: Programação, Algoritmos).
  - **Vocacional:** Dúvida se a área de TI é realmente o que quero para o meu futuro.
  - **Tempo:** Dificuldade extrema em conciliar a carga horária do curso com o trabalho.
</details>

<details>
  <summary><b>3. Sobrecarga Mental</b></summary>

  **De 1 a 5, o quanto o seu nível de estresse ou sobrecarga mental em relação ao curso afeta sua vontade de desistir?**

  - **(1)** Não afeta - Consigo lidar bem com a pressão.
  - **(2)** Afeta pouco - Sinto cansaço, mas é manejável.
  - **(3)** Moderado - O cansaço me faz questionar o curso às vezes.
  - **(4)** Muito - A sobrecarga mental é constante e desmotivadora.
  - **(5)** Extremo - Sinto-me exausto e próximo do meu limite.
</details>

<details>
  <summary><b>4. Impacto de Programas de Suporte</b></summary>

  **Se a instituição oferecesse um programa de suporte, qual teria maior impacto positivo na sua decisão de ficar?**

  - **Apoio Pedagógico:** Monitorias reforçadas e nivelamento em matemática/lógica.
  - **Flexibilidade:** Oferta de disciplinas em regime híbrido ou gravadas.
  - **Carreira:** Parcerias diretas com empresas para estágios e empregos.
  - **Financeiro:** Programas de bolsas, descontos por desempenho ou auxílio-equipamento.
</details>

<details>
  <summary><b>5. Probabilidade de Permanência</b></summary>

  **Qual a probabilidade de você estar matriculado neste mesmo curso daqui a um ano?**

  - **Muito Alta:** Com certeza terminarei o curso.
  - **Alta:** Tenho dificuldades, mas pretendo continuar.
  - **Incerta:** Dependerá de mudanças na minha situação atual ou no curso.
  - **Baixa:** Estou considerando seriamente trancar ou trocar de curso.
  - **Muito Baixa:** Já decidi que não irei continuar.
</details>



## Respostas do Questionário
Clique abaixo para visualizar os gráficos do questionário:

<details>
  <summary><b>Visualizar Gráficos (Perguntas 1 a 5)</b></summary>

  #### Pergunta 1
  [Gráfico 1]<img width="2196" height="996" alt="grafico_Pergunta_1" src="https://github.com/user-attachments/assets/36cbfcdd-49fd-4b88-82ad-2b52e74afc08" />

  #### Pergunta 2
  [Gráfico 2]<img width="2196" height="924" alt="grafico_Pergunta_2" src="https://github.com/user-attachments/assets/afad2135-7893-43e7-872f-aa6bad243c8b" />
  

  #### Pergunta 3
 [Gráfico 3]<img width="2196" height="996" alt="grafico_Pergunta_3" src="https://github.com/user-attachments/assets/49ebb260-8d47-45b3-9ee7-ea73694bf5d6" />

 #### Pergunta 4
 [Grafico 4]<img width="2196" height="996" alt="grafico_Pergunta_4" src="https://github.com/user-attachments/assets/584b76d1-af3f-4ea9-b3b1-c2849601862e" />
 
 #### Pergunta 5
 [Grafico 5] <img width="2196" height="924" alt="grafico_Pergunta_5" src="https://github.com/user-attachments/assets/bdb6745c-ef10-4ac9-a6e6-a5efa93d4821" />

</details>






#  Documentação de Requisitos Funcionais

Este documento detalha as regras e funcionalidades do sistema. Clique em cada item para expandir os detalhes.

---


<details>
  <summary><b>RF01 — Alerta automático de ausências consecutivas</b></summary>

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
</details>

<details>
  <summary><b>RF02 — Upload de diário de frequência pelo professor</b></summary>

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
</details>

<details>
  <summary><b>RF03 — Dashboard de frequência por aluno (visão coordenador)</b></summary>

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
</details>

<details>
  <summary><b>RF04 — Relatório exportável de alunos em risco por turma</b></summary>

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
</details>

<details>
  <summary><b>RF05 — Visão de frequência restrita à disciplina do professor</b></summary>

  ### **Critério de aceitação**
  O professor visualiza apenas:
  - percentual de presença dos alunos
  - dentro da sua própria disciplina

  Nenhum dado de outras disciplinas pode ser acessado:
  - percentual global
  - datas de faltas em outras matérias
  - nomes de outros professores

  ### **Medidas**
  - **0 campos de outras disciplinas** visíveis para professores.
</details>

<details>
  <summary><b>RF06 — Indicador de flexibilidade de oferta por disciplina</b></summary>

  ### **Critério de aceitação**
  O sistema exibe ao coordenador disciplinas com maior índice combinado de:
  - faltas
  - relatos de dificuldade de conciliação com trabalho

  O cruzamento utiliza obrigatoriamente:
  - dados de frequência (**RF02**)
  - relatos dos alunos

  ### **Objetivo**
  Identificar disciplinas candidatas a oferta híbrida ou aulas gravadas. O cruzamento deve ser exibido de forma **agregada** e **sem identificação individual**.

  ### **Medidas**
  - **0 identificações individuais** exibidas ao coordenador.
  - Cruzamento considera obrigatoriamente as **duas fontes de dados**.
</details>

<details>
  <summary><b>RF07 — Painel de oportunidades de estágio e emprego</b></summary>

  ### **Critério de aceitação**
  O sistema exibe oportunidades cadastradas pela coordenação ou parceiros.

  ### **Filtros disponíveis**
  - área
  - modalidade (**presencial/remoto**)
  - carga horária

  ### **Campos obrigatórios da vaga**
  - nome da empresa
  - descrição da vaga
  - requisitos
  - forma de candidatura

  ### **Medidas**
  - **100% das oportunidades** exibem os 4 campos obrigatórios.
</details>

<details>
  <summary><b>RF08 — Configuração de limiares e log de auditoria</b></summary>

  ### **Critério de aceitação**
  O coordenador define o número de faltas consecutivas e o percentual mínimo de presença.

  Toda alteração gera log contendo:
  - data, hora e usuário responsável.

  O log **não pode ser editado nem excluído**.

  ### **Medidas**
  - Log gerado em **100% das alterações**.
  - **0 operações** de edição ou exclusão permitidas.
</details>

<details>
  <summary><b>RF09 — Notificação automática diretamente ao aluno</b></summary>

  ### **Alerta Preventivo**
  Quando a frequência cair abaixo de **85%**.

  ### **Alerta Crítico**
  Quando a frequência cair abaixo de **75%** (risco de reprovação).
  O coordenador também é notificado.

  ### **Medidas**
  - **0 casos sem notificação** ao cruzar os limiares.
  - **100% dos alertas críticos** notificam simultaneamente o coordenador.
</details>

<details>
  <summary><b>RF10 — Autodeclaração voluntária de obstáculo pelo aluno</b></summary>

  ### **Critério de aceitação**
  O aluno indica obstáculos (tempo, financeiro, pedagógico, vocacional).
  A resposta é **anônima por padrão**, exceto se o aluno solicitar contato explicitamente.

  ### **Ação automática**
  Se o aluno selecionar `"vocacional"`, o sistema exibe canais de orientação profissional.

  ### **Notificação ao coordenador**
  O coordenador recebe alerta agregado quando mais de **10% da turma** selecionar `"vocacional"`.

  ### **Medidas**
  - **0 identificações individuais** sem opt-in explícito.
  - Coordenador notificado apenas acima de **10%**.
</details>

---
#  Requisitos Não Funcionais

Esta seção descreve as premissas técnicas, de segurança e de performance do sistema. Clique nos itens abaixo para expandir.

---



<details>
  <summary><b>RNF1 — Privacidade e controle de acesso por perfil (LGPD)</b></summary>

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
</details>

<details>
  <summary><b>RNF2 — Disponibilidade nos períodos críticos</b></summary>

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
</details>

<details>
  <summary><b>RNF3 — Anonimização e separação de dados sensíveis</b></summary>

  Os dados devem ser armazenados separadamente conforme a origem:

  | **Origem** | **Tipo de dado** |
  | :--- | :--- |
  | **RF02** | Frequência acadêmica |
  | **RF10** | Autodeclaração de obstáculos |
  | **RF06** | Relatos de conciliação |

  ### **Regras de Armazenamento**
  - Tabelas de autodeclaração não devem possuir chaves estrangeiras diretas para a tabela de alunos, exceto em casos de *opt-in* confirmado.
  - O cruzamento de dados para o coordenador deve ocorrer em memória/tempo de execução para gerar médias, sem persistir a união dos dados identificáveis.
</details>

---

<details>
<summary><strong>US02 — Alerta Preventivo de Frequência (RF09)</strong></summary>

#User Stories
## Card

Como aluno, eu quero receber uma notificação automática quando minha frequência em uma disciplina cair abaixo de 85%, para que eu possa me organizar a tempo de evitar chegar ao limite mínimo de aprovação.

## Conversation

| Regra | Descrição |
|---------|---------|
| R1 | O alerta é disparado exclusivamente quando a frequência cai abaixo de 85%. |
| R2 | O aluno recebe o alerta no e-mail institucional cadastrado. |
| R3 | O limiar de 85% é configurável pelo coordenador via RF08. |
| R4 | Este alerta é independente do alerta crítico de 75%, tratado na US03. |

## Confirmation

- Quando a frequência do aluno em qualquer disciplina cair abaixo de 85%, o aluno recebe uma notificação preventiva identificando a disciplina e o percentual atual.
- A notificação informa que o limite mínimo para aprovação é 75%.
- Nenhum aluno que cruzar o limiar de 85% deixa de receber a notificação, sendo possível verificar por auditoria de logs.

</details>

<details>
<summary><strong>US03 — Alerta Crítico de Frequência (RF09)</strong></summary>

## Card

Como aluno, eu quero receber uma notificação automática quando minha frequência em uma disciplina cruzar o limite de 75%, para que eu saiba que estou em risco de reprovação direta por falta e o coordenador possa intervir.

## Conversation

| Regra | Descrição |
|---------|---------|
| R1 | O alerta é disparado exclusivamente quando a frequência cruza o limite de 75%. |
| R2 | Além do aluno, o coordenador também é notificado automaticamente. |
| R3 | O limiar de 75% é configurável pelo coordenador via RF08. |
| R4 | Este alerta é independente do alerta preventivo de 85%, tratado na US02. |

## Confirmation

- Quando a frequência do aluno cruzar o limite de 75%, o aluno recebe uma notificação crítica informando o risco de reprovação por falta.
- O coordenador é notificado simultaneamente ao aluno, sem necessidade de ação manual.
- O conteúdo da notificação crítica é textualmente distinto do alerta preventivo da US02.
- Nenhum aluno que cruzar o limiar de 75% deixa de receber a notificação, sendo possível verificar por auditoria de logs.

</details>

<details>
<summary><strong>US04 — Dashboard Consolidado de Frequência (RF03)</strong></summary>

## Card

Como coordenador de curso, eu quero visualizar em um único painel a frequência de todos os alunos por disciplina no semestre vigente, para que eu possa identificar rapidamente quem está em risco sem precisar consultar planilhas separadas.

## Conversation

| Regra | Descrição |
|---------|---------|
| R1 | O dashboard deve refletir os dados mais recentes disponíveis após cada upload de diário. |
| R2 | Nenhum aluno matriculado pode ficar de fora da listagem. |
| R3 | O acesso ao dashboard é restrito ao coordenador. |
| R4 | Esta história cobre apenas a listagem base. Os filtros avançados são tratados na US05. |

## Confirmation

- O dashboard lista 100% dos alunos matriculados no semestre vigente com o percentual de presença por disciplina.
- Alunos com frequência abaixo do limiar configurado são destacados visualmente no painel.
- O dashboard é acessível apenas pelo perfil de coordenador.

</details>

<details>
<summary><strong>US05 — Filtros do Dashboard (RF03)</strong></summary>

## Card

Como coordenador de curso, eu quero filtrar o painel de frequência por turma, disciplina e faixa de frequência de forma combinada, para que eu possa localizar rapidamente grupos específicos de alunos em risco sem percorrer a lista completa.

## Conversation

| Regra | Descrição |
|---------|---------|
| R1 | Os filtros disponíveis são turma, disciplina e faixa de frequência. |
| R2 | Os filtros devem funcionar de forma combinada. |
| R3 | Esta história depende da US04, pois opera sobre a listagem base do dashboard. |

## Confirmation

- Os filtros de turma, disciplina e faixa de frequência funcionam de forma combinada sem erro.
- Ao aplicar qualquer filtro, apenas os alunos que atendem aos critérios selecionados são exibidos.
- Ao remover os filtros, a listagem completa é restaurada sem necessidade de recarregar a página.

</details>
*Documentação de diretrizes técnicas para o projeto.*
