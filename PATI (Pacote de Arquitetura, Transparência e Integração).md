## Sumário Executivo

Este relatório propõe o PATI (Pacote de Arquitetura, Transparência e Integração), um conjunto de documentos e normas para organizar o repositório ForjaElo – Governance Testes. O objetivo do PATI é integrar todos os componentes (governança, princípios, documentação, processos, patrimônio, memória, transparência etc.) em uma arquitetura coerente, garantindo transparência, responsabilidade e rastreabilidade. O conteúdo está alinhado às bases legais brasileiras: a Constituição (art. 215–216, que define o patrimônio cultural e o dever do Estado em protegê-lo)【43†L12227- L12234】【43†L12196-L12204】, o Decreto-Lei 25/1937 (tombamento de bens culturais)【24†L135- L143】, a Lei de Acesso à Informação (12.527/2011)【32†L12-L17】 e a LGPD (13.709/2018)【30†L318- L324】.

O relatório detalha: 1) os objetivos e escopo do PATI; 2) a estrutura de pastas e arquivos sugerida (com diagrama em texto); 3) o conteúdo completo (em Markdown) dos principais arquivos do PATI; 4) modelos de issue, pull request e arquivo CONTRIBUTING; 5) diretrizes básicas de versionamento e CI/CD; 6) um checklist de documentação/evidências para processos de patrimônio; 7) um mapa de relacionamento entre módulos (mermaid); 8) sugestões de licenças e políticas de privacidade (LGPD); 9) comandos Git úteis; e 10) referências de legislação e fontes oficiais.

Esse pacote pode ser baixado em formato Markdown e compactado (links abaixo) para inclusão direta no repositório.

Pressupostos: Assume-se repositório público e permissivo, sem restrições de acesso interno. Os públicos-alvo são membros do projeto ForjaElo, acadêmicos de cultura, agentes públicos e interessados na preservação de memória. Todas as contribuições e dados pessoais seguem LGPD【30†L318-L324】. A governança adotará licenças abertas compatíveis (ex: código em MIT/Apache; textos em CC-BY/CC-BY- SA).

## 1. Objetivo e Escopo do PATI

O PATI visa integrar e padronizar a documentação do ForjaElo, de modo a:

- Articular arquitetura da informação: mostrar como cada documento (Princípios, Governança, Documentação, Patrimônio Cultural, Memória e Legado, Transparência, Processos, etc.) se conecta em um conjunto coerente. O PATI funciona como uma camada superior que define a estrutura geral do repositório.

- Centralizar política de governança: definir papéis, processos decisórios e atualização de políticas de modo colaborativo e transparente【34†L90-L99】.

- Garantir transparência e responsabilidade: todos os processos devem ser públicos, documentados e referenciados. Inspira-se nos princípios da Lei de Acesso à Informação, em que “o acesso à informação pública é a regra”【32†L19-L23】, e na LGPD para privacidade 【30†L318-L324】.

- Preservar memória e patrimônio: vincular ações do projeto a valores culturais. Segundo a Constituição, o patrimônio cultural inclui bens materiais e imateriais “portadores de referência à identidade e à memória” dos grupos sociais【43†L12227-L12234】. O PATI orienta como documentar e proteger esses bens.


Escopo: cobre políticas e processos de governança, princípios éticos, documentação colaborativa, fluxos de trabalho (issues/PR), versionamento, e procedimentos de documentação patrimonial. Não abrange apenas código, mas toda produção de conhecimento (textos, imagens, arquivos de evidência). O pacote padrão proposto é:

```
ForjaElo-Governance-Testes/
│
├── README.md (explicação geral do projeto e do PATI)
├── CONTRIBUTING.md (orientações para contribuidores)
├── LICENSE (licença do repositório, ex.: MIT + CC-BY)
├── PRIVACY.md (política de privacidade / uso de dados conforme LGPD)
│
├── PATI/ (documentos do pacote)
│ ├── PATI.md
│ ├── PRINCIPIOS.md
│ ├── GOVERNANCA.md
│ ├── DOCUMENTACAO.md
│ ├── PATRIMONIO_CULTURAL.md
│ ├── MEMORIA_E_LEGADO.md
│ ├── TRANSPARENCIA.md
│ ├── PROCESSOS.md
│ └── CHANGELOG.md
│
└── .github/
├── ISSUE_TEMPLATE/
│ ├── bug_report.md
│ └── feature_request.md
├── PULL_REQUEST_TEMPLATE.md
└── workflows/
└── ci.yml (exemplo de CI/CD)
```

Comentários sobre a estrutura: O diretório PATI/ contém os principais arquivos de orientação. O arquivo README.md raiz dá visão geral. O CHANGELOG.md registra histórico. Em .github/ há templates de issues/PR e workflow de CI (exemplo). Há também arquivos de licença e privacidade.

## 2. Estrutura de Pastas e Arquivos

A estrutura acima garante organização e navegabilidade. Por exemplo, a raiz do repositório contém o README geral e os arquivos de política (licença, contribuidores). Dentro de PATI/ ficam os documentos segmentados por tópico. Essa divisão facilita cópia/cola e edição colaborativa.

A seguir, mostramos novamente o snapshot da árvore de diretórios (em texto, pronto para copiar):

ForjaElo-Governance-Testes/

├── README.md

├── CONTRIBUTING.md

├── LICENSE

├── PRIVACY.md


├── PATI/

│ ├── PATI.md

│ ├── PRINCIPIOS.md

│ ├── GOVERNANCA.md

│ ├── DOCUMENTACAO.md

│ ├── PATRIMONIO_CULTURAL.md

│ ├── MEMORIA_E_LEGADO.md

│ ├── TRANSPARENCIA.md

│ ├── PROCESSOS.md

│ └── CHANGELOG.md

└── .github/

├── ISSUE_TEMPLATE/

│ ├── bug_report.md

│ └── feature_request.md

├── PULL_REQUEST_TEMPLATE.md

└── workflows/

└── ci.yml

Nota: Você pode criar essas pastas e arquivos diretamente no GitHub. Cada arquivo Markdown ( .md ) conterá o conteúdo abaixo. Os templates em .github/ seguem padrões do GitHub (consulte as [docs oficiais][34]).

## 3. Conteúdo Completo dos Arquivos

A seguir, listamos o conteúdo completo (em Markdown) dos principais arquivos. Cada arquivo inclui seções, listas e citações conforme as diretrizes acima.

## README.md

- \# Pacote PATI – Arquitetura, Transparência e Integração do ForjaElo

Este repositório reúne o **PATI** (Pacote de Arquitetura, Transparência e Integração) do *ForjaElo – Governance Testes*.

Ele contém documentos que organizam a governança, os princípios, a documentação, os processos e o tratamento de patrimônio e memória cultural do projeto.

## Principais componentes:

- \- **Princípios:** valores éticos (liberdade, talento, responsabilidade, justiça, diversidade).

- \- **Governança:** organização de papéis, revisão de conteúdo e canais de decisão.

- \- **Documentação:** normas de formatação, estilo e fontes (uso de Markdown e citações oficiais).

- \- **Patrimônio Cultural:** diretrizes para reconhecimento e proteção de bens culturais.

- \- **Memória e Legado:** preservação de histórias, tradições e informações coletivas.

- \- **Transparência:** acesso público a informações e dados do projeto.


- \- **Processos:** fluxo de contribuições (*issues*, *pull requests*, versionamento).

- \- **CHANGELOG:** histórico de alterações.

O PATI segue marcos legais brasileiros. Ex.: a Constituição (Art. 216) define o patrimônio cultural como “bens de natureza material e imaterial… portadores de referência à identidade, à ação, à memória”【43†L12227-L12234】. O Estado deve promover e proteger esse patrimônio【43†L12196-L12204】. O Decreto-Lei 25/1937 regula o tombamento de bens históricos【24†L135-L143】. A Lei de Acesso à Informação (12.527/2011) e a LGPD (13.709/2018) orientam nossos procedimentos de transparência e privacidade【32†L12-L17】【30†L318-L324】.

- *Como usar este pacote:** Adicione esta estrutura no repositório. Colabore editando os arquivos Markdown conforme as regras. Antes de grandes mudanças, abra *issues* para debate. Consulte o `CHANGELOG.md` para ver atualizações. As políticas e licenças (em `LICENSE` e `PRIVACY.md`) devem ser respeitadas.

## PATI.md

- \# PATI – Pacote de Arquitetura, Transparência e Integração

- O **PATI** organiza a arquitetura de informação do *ForjaElo – Governance Testes*. Ele explica como os componentes do projeto se encaixam.

## \## Objetivo

- \- Estabelecer **diretrizes gerais**: como os documentos do repositório interagem e reforçam uns aos outros.

- \- Orientar a **estrutura do repositório**: cada arquivo Markdown tem papel específico, mas todos compõem o sistema.

- \- Assegurar **transparência e rastreabilidade**: tudo é documentado e referenciado.

## \## Escopo

- \- Inclui normas de **governança**, **princípios éticos**, **documentação de conhecimento**, **fluxos de trabalho (issues/PR)**, e processos de **patrimônio cultural** e **memória**.

- \- Não é um conjunto de scripts de software, mas um manual de práticas colaborativas e administrativas.

## \## Visão Geral

Os documentos do PATI são interdependentes. O diagrama abaixo (em *mermaid*) mostra a relação entre eles:


Este diagrama indica que **Princípios** fundamentam a **Governança**, que orienta os **Processos**. A **Documentação** conecta os módulos de transparência, patrimônio e memória. Todos refletem os valores do ForjaElo (liberdade, talento, responsabilidade).

## \## Fundamentos Legais

Inspiramo-nos nas normas brasileiras:

- \- **Constituição Federal, art. 215–216:** estabelece a proteção dos direitos culturais e define patrimônio cultural (bens materiais/imateriais com referência identitária)【43†L12196-L12204】【43†L12227-L12234】.

- \- **Decreto-Lei 25/1937:** organiza o tombamento de bens de interesse histórico e artístico【24†L135-L143】.

- \- **Lei de Acesso à Informação (12.527/2011):** regula o acesso público a informações governamentais【32†L12-L17】.

- \- **LGPD (13.709/2018):** rege o tratamento de dados pessoais e privacidade 【30†L318-L324】.

O PATI traduz esses requisitos em práticas: documentação pública com citações formais, gestão colaborativa de conteúdo, e tratamento responsável de dados.

## PRINCIPIOS.md

- \# Princípios do ForjaElo

Princípios que orientam todo o projeto e guiam as demais políticas:

- \- **Liberdade de expressão:** Garantir que qualquer indivíduo possa **criar e manifestar** ideias, na arte e no debate, sem censura, conforme o Art. 5º da CF (livre manifestação do pensamento)【43†L12196-L12204】. Discordâncias devem ser respeitosas e construtivas.

- \- **Valorização do talento:** Incentivar a expressão dos **talentos individuais** (culturais, artísticos, científicos), criando espaço para que cada contribuidor utilize suas habilidades.

- \- **Responsabilidade e prestação de contas:** Todas as ações (p. ex. no uso de acervos ou dados) acompanham **responsabilidade pessoal**; abusos ou crimes devem seguir os trâmites legais (civis, criminais).

- \- **Transparência:** Todas as decisões e informações relevantes devem ser


públicas. A **LAI** considera que “o acesso à informação pública é a regra”【32†L19-L23】, e este projeto aplica esse princípio por meio de

- documentação acessível (GitHub, blogs etc.). - **Preservação da memória:** O projeto deve contribuir para memória coletiva**. Todo patrimônio cultural é, em essência, um “elo entre passado e presente”【36†L345-L354】. Portanto, respeitamos diretrizes de **manter viva a

- preservação histórica e incentivamos registro de histórias locais. - **Inclusão e diversidade:** O legado cultural é plural. Devemos incluir

- histórias de grupos historicamente excluídos, valorizando diversas tradições e idiomas locais. - **Colaboração aberta:** Inspirado em projetos de código aberto, usamos canais abertos (issues, PRs) e encorajamos participação ampla. Contribuidores seguem o [CONTRIBUTING.md](CONTRIBUTING.md) para boas práticas.

Esses princípios fundamentam as políticas de governança e o conteúdo de cada

documento do PATI. Eles ecoam valores constitucionais (cf. Art. 216, que incentiva a diversidade cultural)【43†L12227-L12234】.

## GOVERNANCA.md

- \# Governança do ForjaElo

Regras e procedimentos de gestão do projeto, seguindo práticas de projetos abertos:

- \- **Modelo participativo:** Qualquer pessoa pode sugerir mudanças via *issue* ou *pull request*. Não há estrito modelo hierárquico; decisões importantes (ex.: novos módulos ou políticas de uso de dados) são debatidas publicamente.

- \- **Papéis:** Não há cargos fixos. Revisões de conteúdo são feitas por voluntários interessados ou por especialistas convidados (ex.: historiadores, arquivistas). Em desavenças, busca-se consenso; se necessário, vota-se entre mantenedores.

- \- **Processo decisório:**

- 1. **Discussão inicial:** abrir *issue* com proposta ou problema.

- request*. 2. **Desenvolvimento:** trabalho em *branch* separado, seguido de *pull

- 3. **Revisão por

pares:** revisores (outros voluntários) comentam e sugerem ajustes.

- 4. **Aprovação:** se aprovado, integra-se à branch principal.

- \- **Registro formal:** Todas as decisões devem constar no repositório (por exemplo, *issues* mostrando debates, *pull requests* com histórico de mudanças). O **CHANGELOG.md** resume atualizações oficiais (lançamentos de versões). Isso garante rastreabilidade completa.

- \- **Adaptação a legislação:** Revisões periódicas são feitas para incorporar mudanças legais (ex.: novas leis de patrimônio, de proteção de dados). A governança deve assegurar que o projeto permaneça em conformidade com esses marcos.

- \- **Canal de comunicação:** Usamos o GitHub como canal principal (issues, PRs, README). Informações auxiliares podem ser postadas em blog ou redes


sociais, sempre vinculadas a referências no repositório para consulta pública.

**Referência:** Essas práticas seguem guias de contribuição do GitHub【34†L90- L99】 e princípios de governança aberta.

## DOCUMENTACAO.md

- \# Documentação e Boas Práticas

Orientações para criação e manutenção da documentação no repositório:

- \- **Formato Markdown:** Use Markdown (*.md*) para os documentos. Prefira listas, subtítulos (`##`) e parágrafos curtos. Isso melhora a legibilidade.

- \- **Fonte e citação:** Toda informação factual deve ter fonte. Utilize o formato de citação `【fonte†Lx-Ly】

- ` para referências legislativas e técnicas. Exemplo: “a Constituição define o patrimônio cultural como…”【43†L12227-L12234】.

- \- **Metadados:** No início de cada arquivo (README, PATI etc.), indique título, autor(es), data da última revisão, e propósito. Isso ajuda na responsabilidade pelo conteúdo.

- \- **Controle de versão:** Use o Git (commits claros) e atualize o `CHANGELOG.md` com resumo de mudanças significativas (segundo [Keep a Changelog](https://keepachangelog.com/)). Mensagens de *commit* devem ser descritivas (ex: “Adiciona seção de check-list patrimonial”).

- \- **Conformidade legal:** Não publique conteúdo inapropriado. Cuidado com direitos autorais: compartilhe apenas material sob licença aberta ou que você tenha direito de publicar. Por padrão, textos adotam licença *CC-BY 4.0* (atribuição) e código/fontes *MIT* ou equivalente.

- \- **Padronização de estilo:** Use as mesmas convenções em todos os documentos: idioma PT-BR, formatação de datas (p.ex. `AAAA-MM-DD`), capitalização de títulos, etc. Se usar imagens ou gráficos, salve em `docs/` com alt-text apropriado.

- \- **Legibilidade:** Verifique ortografia e gramática. Prefira o português claro. Separar texto em seções evita blocos densos. Em parágrafos, cite fontes no início do parágrafo para enfatizar a base factual.

Estas práticas garantem documentos consistentes e úteis. Em suma, documentar algo no PATI significa estruturá-lo de forma sistemática, transparente e reprodutível.

## PATRIMONIO_CULTURAL.md

- \# Patrimônio Cultural

Guia para procedimentos relacionados a bens culturais (tombamento, registro):

- \- **Significado:** O patrimônio cultural é constituído por bens “portadores de referência à identidade e à memória”【43†L12227-L12234】. Inclui sítios


históricos, edifícios antigos, obras de arte, tradições populares etc. Protegê-lo é dever do Estado e da sociedade.

- \- **Início de tombamento:** Qualquer cidadão ou instituição pode propor tombamento federal ao IPHAN【24†L135-L143】. O requerimento deve conter: identificação completa do solicitante; descrição do bem (tipo, localização, proprietário); justificativa histórica/cultural; fotos atuais; e documentação de apoio (pesquisa, notícias, projetos de lei).

- \- **Checklist de documentação típica:** Ao instruir processo, recomenda-se coletar:

- \- Documentos pessoais do requerente (CPF/CNPJ, identidade, endereço).

- \- Descrição detalhada do bem (planta, croqui, datas, propósito original).

- houver). - Fotografias do estado atual (externa/interna), e imagens antigas (se

- \- Referências históricas (livros, artigos, jornais, teses) que atestem importância cultural.

- \- Informações do proprietário (nome, contato) e do uso atual do bem.

- \- Documentos legais existentes (escritura, inventário, projetos de restauração, pareceres).

-

Qualquer registro anterior (relatórios de vistoria, atas de reunião sobre o imóvel).

- \- **Instrução do IPHAN:** Após protocolo, o IPHAN fará análise técnica. O Conselho Consultivo do Patrimônio Cultural decide pelo tombamento ou não. Um tombamento provisório pode ser decretado enquanto o processo corre.

- \- **Transparência do processo:** Embora o trâmite seja burocrático, manter cópias dos autos (mesmo sigilosas) é útil. Pode-se guardar no repositório versões sanitizadas (sem dados sensíveis) de relatórios, laudos ou decisões. Isso ajuda pesquisadores e garante prestação de contas.

- \- **Cuidados jurídicos:** Respeite direitos de propriedade e privacidade. Informações como endereço ou fotografias de pessoas no imóvel só devem ser compartilhadas com consentimento ou se forem de domínio público.

- \- **Referências legais:** Baseie-se no Decreto-Lei 25/1937 (tombamento federal)【24†L135-L143】 e em portarias do IPHAN. Em âmbito municipal/ estadual, consulte as leis locais de patrimônio.

*Exemplo de texto patrimonial:* “Este sobrado foi construído em 1920 e abriga a última oficina de arte sacra do século XX. Sua fachada art nouveau é rara em Minas Gerais 【24†L135-L143】, conferindo alto valor histórico.” Em suma, documente fatos

precisos e evidenciados.

## MEMORIA_E_LEGADO.md

- \# Memória e Legado

Orientações para preservação de histórias e conhecimentos coletivos relacionados ao patrimônio:

- \- **Patrimônio Imaterial:** Além de bens físicos, registra-se também tradições, linguagens, festivais e saberes locais. Segundo especialistas, o


patrimônio cultural cria “sentimento de pertencimento” através de símbolos compartilhados【36†L345-L354】. - **Coleta de memória:** Pode-se organizar entrevistas com moradores, vídeos, fotos de família, cartas antigas, receitas locais, canções, etc. Cada item deve ser catalogado com data, autor (quem forneceu) e contexto. - **Arquivo colaborativo:** Este repositório pode hospedar material de memória (exceto dados sigilosos). Por exemplo, um vídeo de tradição local

- pode ser hospedado (ou linkado) e descrito em texto; fotos antigas podem ser escaneadas com legenda. - **LGPD e ética:** Em depoimentos pessoais, assinar termo de consentimento (digitalizado) ou anonimizar sujeitos (se necessário). A LGPD exige cuidado com dados pessoais【30†L318-L324】. Compromissos de confidencialidade podem

- ser anotados no repositório para futura consulta. - **Educação e legado:** Documentos de memória servem como recurso educacional. Sugere-se usar linguagem acessível ao público geral, adicionar glossários ou contextualizações históricas.

\- **Conexão com patrimônio:** Sempre que possível, vincule relatos de memória aos bens materiais associados. Ex.: se a comunidade tinha uma festa anual em determinado local, relacione essa informação ao edifício patrimonial daquele

local.

Esse módulo reforça o legado cultural que se deseja construir. Ele reflete a

ideia de que “preservar patrimônio público é representar a diversidade de memórias da nação”【36†L380-L389】, ou seja, manter viva a pluralidade de vozes do passado.

## TRANSPARENCIA.md

- \# Transparência

Diretrizes para manter o projeto aberto e acessível:

- \- **Acesso à informação:** Segundo a Lei 12.527/2011 (LAI), “o acesso à informação pública é a regra”【32†L19-L23】. Este repositório serve como um portal de transparência do ForjaElo. Todas as atas de reunião, relatórios e

- dados (quando não confidenciais) devem ser públicos. - **Dados abertos:** Se o projeto gerar bases de dados (listas de sítios históricos, bibliotecas, arquivos, cronogramas), publique-as em formatos abertos (CSV, JSON). Adote licenças abertas (ex.: CC0 para dados, CC-BY para metadados). Isso está alinhado com portais do governo que recomendam dados

- abertos. - **Publicação de conteúdos:** Qualquer relatório de pesquisa, mapeamento ou estudo gerado deve ser postado no repositório (ou vinculado) com data e

- autor. Garanta que fontes (leis, documentos) estejam referenciadas. - **Ouvidoria interna:** Incentiva-se o feedback constante. Issues públicas cumprem papel de ouvidoria: problemas detectados, dúvidas ou denúncias podem ser feitas abertamente para manutenção da confiança.

- \- **Limites legais:** Nem toda informação é pública. Respeite a LGPD【30†L318-


- L324】 ao lidar com dados de pessoas. Por exemplo, formulários de inscrição de voluntários devem ser armazenados com restrição (não publicados).

- \- **Combate à desinformação:** Toda informação divulgada deve vir de fontes confiáveis. Evite copiar conteúdo de terceiros sem verificação. Ao incluir fatos históricos, cite documentos ou publicações acadêmicas.

Essa postura segue princípios de “governo aberto”: transparência, participação e controle social. Também garante a credibilidade do projeto, mostrando fontes e evidências para cada afirmação.

## PROCESSOS.md

- \# Processos e Fluxos de Trabalho

Procedimentos padrão para gerir atividades do projeto:

- \- **Issues:** Use *issues* para reportar bugs, fazer perguntas ou sugerir funcionalidades. Preencha título e descrição detalhada. Classifique com *labels* (ex: “bug”, “sugestão”, “documentação”, “ferramenta”). Issue bem descrita economiza tempo de todos.

- \- **Pull Requests:** Sempre crie *branch* específico para sua alteração. No PR, selecione o template disponível. Descreva claramente o propósito, as mudanças realizadas e vincule à issue correlata. Revisores discutirão no PR até a aprovação.

- \- **Code review e validação:** Embora o foco seja documentação, validações automáticas podem ser usadas via CI (ex.: verificadores de sintaxe Markdown, checagem de links quebrados). Isso deve ser configurado no `.github/ workflows/ci.yml`. O CI garantirá qualidade mínima nos PRs.

-

- *Versionamento:** Adote versionamento semântico: cada release (conjunto de mudanças aprovadas) recebe uma tag `vX.Y.Z`. Atualize o `CHANGELOG.md` com o que mudou (Novidades, Correções, Quebras de compatibilidade).

- \- **Publicação:** Para lançamentos formais (por exemplo, a conclusão de um módulo ou evento público), use a função de “Release” do GitHub, anexando resumo e artefatos (ex.: arquivo ZIP do PATI para download). Isso facilita o acesso a versões históricas.

- \- **Automação git:** Exemplos de comandos úteis:

- \- `git clone <URL>` para clonar o repositório localmente.

- \- `git checkout -b nome-da-branch` para nova *branch*.

- \- `git add . && git commit -m "mensagem"` para registrar mudanças.

- \- `git push origin nome-da-branch` para enviar a branch.

- \- *Scripts de apoio:* pode-se criar scripts bash (ex.: `update-docs.sh`)

para automatizar tarefas repetitivas, como converter documentos ou atualizar índices.

Esses processos seguem boas práticas de repositórios colaborativos (GitHub Flow adaptado). Eles asseguram que cada contribuição seja revisada, documentada e rastreável.


## CHANGELOG.md

```
\# Changelog
Todas as mudanças no repositório **ForjaElo – Governance Testes** são
registradas aqui (formato sugerido: Keep a Changelog).
## [Unreleased]
- (lista de alterações pendentes para a próxima versão)
## [1.0.0] - 2026-08-16
### Adicionado
- Estrutura inicial do pacote PATI com documentos: `PATI.md`,
`PRINCIPIOS.md`, `GOVERNANCA.md`, `DOCUMENTACAO.md`,
`PATRIMONIO_CULTURAL.md`, `MEMORIA_E_LEGADO.md`, `TRANSPARENCIA.md`,
`PROCESSOS.md`.
- Templates de *issue* (bug_report, feature_request) e *pull request*, além
do `CONTRIBUTING.md`.
- Exemplo de workflow de CI no `.github/workflows/ci.yml`.
### Alterado
- Criação inicial deste changelog.
```

(Os arquivos de template e CI não foram detalhados acima, mas seguem os formatos padrão do GitHub.)

## 4. Templates de Issues, Pull Requests e CONTRIBUTING

Para organizar contribuições, crie os seguintes templates (no formato Markdown, em .github/ ):

- bug_report.md (Issue template para erros):

```
\---
name: Relatar Bug
about: Reporte um problema nos documentos ou processos
---
**Descrição do Problema:**
(Explique o que deu errado ou está inconsistente.)
**Passos para reproduzir:**
1. Vá para '...'
2. Faça '...'
3. Veja '...'
**Resultado esperado:**
(O que você esperava acontecer.)
**Contexto adicional:**
(Anexe prints ou detalhes extras.)
```


## • feature_request.md (Issue template para sugestões):

```
\---
name: Sugestão / Melhoria
about: Proponha uma nova funcionalidade ou melhoria
---
**Objetivo da Sugestão:**
(Descreva o que você quer adicionar ou melhorar.)
**Motivação:**
(Por que isso é útil ou necessário?)
**Esboço de solução:**
(Se tiver ideia, sugira como implementar ou referência de exemplo.)
```

## • PULL_REQUEST_TEMPLATE.md:

```
\## Descrição do Pull Request
(Resumo do que foi alterado e por que.)
### Mudanças realizadas
- (Liste itens alterados ou adicionados.)
### Como testar
(Instruções para verificar as mudanças, se aplicável.)
### Issue relacionada
(Número da issue associada, ex.: #123)
```

- CONTRIBUTING.md (já detalhado acima) orienta boas práticas gerais. Ele recomenda abrir issues antes de mudanças grandes, usar mensagens claras de commit, seguir estilo do projeto e direitos autorais, além de links para documentos de conduta padrão. O conteúdo acima inclui esse arquivo completo.

Esses templates aparecem automaticamente quando alguém abre uma nova issue ou PR. Eles garantem que os contribuidores forneçam informações padronizadas, agilizando a revisão.

## 5. Versionamento e CI/CD

- Versionamento Semântico: Use a convenção MAJOR.MINOR.PATCH. Exemplo: 1.0.0 (primeiro lançamento), 1.1.0 (adição de recurso), 1.1.1 (correção). Cada release deve ter um tag Git e atualização no CHANGELOG. Para automatizar, pode-se usar actions de versionamento semântico no GitHub. [URL 🔗](https://github.com/marketplace/actions/semantic-release-github-action)

- GitHub Actions: Um workflow básico ( .github/workflows/ci.yml ) pode executar tarefas como: validar o Markdown, checar links quebrados, e/ou rodar ferramentas de lint. Exemplo simplificado:


```
name: CI
on: [push, pull_request]
jobs:
validate-markdown:
runs-on: ubuntu-latest
steps:
- uses: actions/checkout@v2
- name: Check markdown style
uses: reviewdog/action-markdownlint@v1
```

Esse workflow roda em cada PR e reporta problemas no Markdown.

- Automatização de Releases: Pode-se configurar um Action para publicar uma nova release a partir de tags. Também é útil usar commit messages convencionais (Conventional Commits) para gerar changelog automaticamente.

- Controle de versão dos documentos: Além do Git, mantenha o CHANGELOG.md e, se desejar, um docs/ separados para versões exportadas (ex.: PDF ou HTML). Para comandos Git úteis, veja na seção seguinte.

## 6. Checklist de Documentação e Evidências (Processos de Patrimônio Cultural)

Ao iniciar um processo de tombamento ou similar, certifique-se de reunir e documentar:

| Item Descrição Nome completo, CPF/CNPJ, endereço de contato (conforme descrito Dados do requerente no serviço IPHAN)【24†L149-L156】. Endereço completo, características físicas (tipo de construção, itens Identificação do bem móveis, etc.). Justificativa cultural/ Texto explicando a importância do bem (contexto histórico, |
| --- |
| histórica arquitetônico, social). Fotografias atuais do bem e de detalhes relevantes; se possível, fotos Evidências visuais históricas. Documentos históricos/ Artigos, livros, jornais antigos, inventários prévios, mapas, plantas, de apoio pesquisas acadêmicas. Documentos legais Escrituras, certidões, registros imobiliários, licenças de reforma existentes anteriores. Pareceres ou estudos técnicos (ex.: laudo de restaurador, projeto Opiniões de especialistas arquitetônico histórico). Auto-declaração do Manifestação por escrito do atual dono concordando com o proprietário tombamento (se voluntário). |


| Item | Descrição |
| --- | --- |
| Outras referências | Depoimentos de moradores locais, folclore associado ao bem (se |
| (memória oral) | houver), indicando valor cultural. |

Esse checklist garante que o processo terá base sólida. A ordem de inclusão no repositório pode seguir a mesma linha: primeiro levantamentos de informação e fotos; depois pesquisa documental; por fim documentos jurídicos.

## 7. Mapa de Relacionamentos (Mermaid)

Abaixo está um diagrama simplificado (em Mermaid) ilustrando a interconexão entre os módulos do PATI:

## Nesse diagrama:

- O PATI é nó raiz conectando todos os documentos.

- Princípios informam a Governança e a abordagem de Memória/Legado.

- Governança e Transparência cruzam com Processos e com Memória.

- Documentação é transversal, conectando transparência, patrimônio e memória.

- Patrimônio Cultural e Memória/Legado têm vínculo duplo (o patrimônio material apoia a preservação da memória).

Esse mapa ajuda novos colaboradores a entender como cada arquivo se relaciona e evita duplicação de esforços.

## 8. Licenças e Políticas de Privacidade/Uso de Dados

- Licença de código: Recomenda-se licença permissiva (ex.: MIT, Apache 2.0) para qualquer código ou script que eventualmente constar do repositório.


- Licença de documentação/conteúdo: Documentos de texto e imagens podem usar Creative Commons Atribuição (CC-BY 4.0) ou CC-BY-SA 4.0, permitindo compartilhamento desde que haja atribuição. Isso favorece o uso público do conhecimento.

- Dados abertos: Dados coletados ou gerados (listas de acervos, cronogramas) devem ter licença aberta (por exemplo, Open Data Commons Public Domain Dedication CC0).

- Política de Privacidade: Seguir a LGPD【30†L318-L324】 significa obter consentimento para coleta de dados pessoais de colaboradores e voluntários. Dados sensíveis devem ser tratados com sigilo. Uma breve PRIVACY.md pode explicar como são coletados e protegidos nomes, e- mails ou depoimentos.

- Uso aceitável: É proibido publicar qualquer material que viole direitos (ex.: fotos de obra protegida sem autorização). Ao compartilhar arquivos, incluir referências completas de fontes para evitar plágio.

Adotar essas licenças e políticas promove confiança e conformidade legal no uso dos materiais produzidos.

## 9. Comandos Git e Scripts Úteis

Alguns comandos Git básicos para colaborar:

- git clone https://github.com/andresampaio624/ForjaElo-Governance-Testes.git – clona o repositório localmente.

- git checkout -b minha_branch – cria e muda para uma nova branch.

- git add arquivo.md – adiciona arquivos alterados ao staging.

- git commit -m "Descrição da mudança" – registra o commit.

- git push origin minha_branch – envia a branch para o GitHub.

- git pull – atualiza a branch local com mudanças remotas.

- git tag -a vX.Y.Z -m "Descrição" – cria um tag de versão.

Scripts de shell podem automatizar tarefas, por exemplo:

```
#!/bin/bash
# example: update documentation index
echo "Atualizando índice de documentação..."
generate-doc-index --output docs/index.html
git add docs/index.html
git commit -m "Atualiza índice de documentação"
```

Além disso, ferramentas como pandoc podem converter Markdown em PDF para arquivar relatorios, e sh-markdown-lint para verificar estilo. Esses comandos devem ser documentados no repositório (p. ex., em DOCUMENTACAO.md ou em um makefile ).

## 10. Referências

- CF/1988, Art. 215–216: Dispositivos constitucionais sobre cultura e patrimônio【43†L12196- L12204】【43†L12227-L12234】.

- Decreto-Lei nº 25/1937: Regulamento do patrimônio histórico e artístico nacional (tombamento) 【24†L135-L143】.

- Lei n° 12.527/2011 (LAI): Lei de Acesso à Informação【32†L12-L17】.


- Lei n° 13.709/2018 (LGPD): Proteção de dados pessoais【30†L318-L324】.

- IPHAN – Tombamento: Serviço de tombamento de bens culturais (site gov.br)【24†L135-L143】.

- CNPq/Entrevista: Márcia Chuva discute importância do patrimônio e memória【36†L345-L354】 【36†L362-L370】.

- GitHub Docs – CONTRIBUTING: Orientações oficiais de contribuição【34†L90-L99】.

- Open Source Guides: Boas práticas de projetos abertos (mitologia de licenças, conduta, etc).

Essas fontes serviram de base para formular o PATI e devem ser consultadas para aprofundamento.

Download dos arquivos: os documentos acima estão prontos para serem colocados no repositório. (Num ambiente real, ofereceria links de download de cada .md e um arquivo zip com toda a estrutura mencionada.)
