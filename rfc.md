# Capa

- **Título do Projeto**: Synk, a melhor forma de padronizar seus anúncios e divulgações.
- **Nome do Estudante**: Cristian Prochnow.
- **Curso**: Engenharia de Software.
- **Data de Entrega**: ...

# Resumo

Gerenciar a comunicação em múltiplas plataformas sociais é uma tarefa repetitiva e demorada. Equipes de marketing perdem tempo postando manualmente em cada rede, enquanto times de desenvolvimento lutam para comunicar atualizações de forma ágil e consistente.

Synk surge como a solução para este desafio. Nossa plataforma centraliza e automatiza a publicação de conteúdo, permitindo que você economize tempo e mantenha a consistência da sua marca.

Através de um sistema intuitivo de **templates** e **integrações diretas** com as principais redes sociais, o Synk transforma um processo de vários passos em um único clique. Crie seus modelos de posts para diferentes contextos — seja um lançamento de produto, uma campanha de marketing ou uma nota de atualização — e publique simultaneamente onde seu público estiver.

É importante ressaltar: o Synk não é um CRM. Nosso foco é ser uma ferramenta especialista em agilidade, eliminando o esforço manual e repetitivo para que sua equipe possa se concentrar no que realmente importa: a estratégia e a criação de conteúdo de valor.

## 1. Introdução

No cenário digital atual, a presença constante e a interação ágil com o público são cruciais para o sucesso de qualquer empresa. No entanto, o processo para manter essa comunicação ativa — através de posts, anúncios e atualizações — é frequentemente manual, repetitivo e consome um tempo valioso das equipes.

O Synk foi criado para eliminar esse gargalo. Nossa plataforma ataca diretamente as tarefas que, embora pareçam triviais, são volumosas e desgastantes: a criação e publicação manual de conteúdo em diversas plataformas.

Nosso objetivo é simples: fornecer uma interface centralizada onde você pode criar e salvar templates para qualquer tipo de comunicado. Precisa anunciar uma atualização de produto no Slack e no Twitter? Preparar um post comercial para o LinkedIn? Com o Synk, você seleciona o modelo, faz ajustes rápidos e publica em todas as redes desejadas com poucos cliques.

É importante notar que o Synk não é um CRM. Nosso foco exclusivo é otimizar a base da sua produtividade, devolvendo o tempo que seria gasto em tarefas manuais para que sua equipe possa se concentrar em estratégia e crescimento.

## 2. Descrição do Projeto

O Synk é uma plataforma centralizadora projetada para otimizar a criação e publicação de conteúdo em múltiplas redes sociais e canais de comunicação. A ferramenta permite que usuários gerenciem uma biblioteca de templates, customizem textos de forma intuitiva e, após a configuração das integrações, publiquem em diversas plataformas com um único comando.

O projeto nasceu para resolver um desafio comum e frustrante: a necessidade de adaptar e postar manualmente o mesmo conteúdo em diferentes canais, um processo repetitivo que consome tempo e abre margem para inconsistências. O Synk elimina essa fricção ao permitir que templates sejam pré-configurados para contextos e redes específicas, unificando todo o fluxo de publicação.

É crucial entender nosso foco estratégico: diferente de plataformas de CRM que oferecem um leque amplo de funcionalidades, incluindo análise de métricas, o Synk se especializa na etapa de **execução**. Nosso objetivo é ser a melhor ferramenta para o trabalho prático de criar e distribuir conteúdo, atacando a tarefa que, embora muitas vezes considerada trivial, é a que mais consome tempo no dia a dia.

## 3. Especificação Técnica

### 3.1. Resumo

O sistema Synk é uma plataforma multiusuário (multi-tenant) para a criação, gerenciamento e publicação de conteúdo em redes sociais, baseada em um sistema de templates e integrações com APIs de terceiros.

### 3.2. Componentes Principais do Sistema

1. **Módulo de Usuários (Identity & Access Management)**
    - Responsável pelo cadastro, login (autenticação) e controle de permissões (autorização) dos usuários.
2. **Módulo de Templates**
    - Permite operações de CRUD (Criar, Ler, Atualizar, Excluir) para os templates de posts.
    - Cada template é estritamente vinculado ao usuário que o criou.
3. **Módulo de Integrações**
    - Gerencia as configurações e credenciais (tokens, chaves de API) para cada plataforma de destino (ex: LinkedIn, Twitter, Slack).
    - Deve garantir o armazenamento seguro das informações sensíveis.
4. **Módulo de Publicação (Publishing Engine)**
    - Utiliza um template e uma ou mais integrações ativas para realizar a postagem do conteúdo através das APIs correspondentes.
    - Responsável por tratar as respostas (sucesso/erro) de cada API.
5. **Módulo de Importação (Content Importer)**
    - Processa uma URL de um post público para extrair seu conteúdo e popular os campos de um novo template.
6. **Editor de Conteúdo (Rich Text Editor)**
    - Fornece uma interface de usuário (UI) do tipo WYSIWYG ("What You See Is What You Get") para que os usuários possam formatar o texto dos templates com estilos (negrito, itálico, listas, etc.).

### 3.1. Requisitos de Software
- Apresentar os requisitos do tema proposto.
- **Lista de Requisitos:** Apresentar uma lista contendo os Requisitos Funcionais (RF) e Não-Funcionais (RNF).
- **Representação dos Requisitos:** Representar os RFs por meio de um Diagrama de Casos de Uso (UML).

#### 3.1.1. Requisitos Funcionais

* RF001. O sistema deve permitir o cadastro de usuários por meio dos dados de nome, e-mail e senha
* RF002. O sistema deve enviar e-mail de autenticação para validação de novos usuários, com um link clicável que servirá como confirmação da nova conta criada
* RF003. O sistema deve permitir a edição dos dados do perfil do usuário como nome e senha, exigindo confirmação adicional para o segundo e também alteração da foto de perfil
* RF004. O sistema deve validar o arquivo enviado como foto de perfil, restringindo pelo tamanho de arquivo (2mb) ou formato enviados (png, jpg, gif).
* RF005. O sistema deve permitir a inativação dos dados do usuário, caso desejado
* RF006. O sistema deve permitir a exclusão total dos dados do usuário caso requerido expressamente pelo usuário
* RF007. O sistema deve permitir a criação de novos templates de _post_, exigindo então um nome para o template e o conteúdo desejado em texto
* RF008. O sistema deve permitir a importação de conteúdo de texto por meio de URLs inseridas na aplicação durante a criação de novos templates
* RF009. O sistema deve permitir a publicação dos templates, oferecendo a possibilidade da edição de conteúdo e também a seleção de quais as redes destino
* RF010. O sistema deve permitir a integração com as plataformas que estarem disponíveis, realizando o processamento quando selecionado em um template
* RF011. O sistema deve permitir o cadastro de perfis de integração, relacionando credenciais de acesso às plataformas conforme o contexto específico de criação
* RF012. O sistema deve permitir a seleção de perfil de integração ao publicar um template
* RF013. O sistema deve agrupar os dados de acesso conforme os perfis de integração cadastrados pelo usuário
* RF014. O sistema deve permitir o gerenciamento de credenciais de acesso para as integrações das plataformas disponíveis de integração
* RF015. O sistema deve permitir a inativação dos templates desejados, jogando-os para a lixeira com a possibilidade de resgate do template caso desejado

#### 3.1.2. Requisitos Não-Funcionais

### 3.2. Considerações de Design

#### 3.2.1. Visão inicial

- Discussão sobre as escolhas de design, incluindo alternativas consideradas e justificativas para as decisões tomadas.
- **Visão Inicial da Arquitetura**: Descrição dos componentes principais e suas interconexões.
- **Padrões de Arquitetura**: Indicação de padrões específicos utilizados (ex.: MVC, Microserviços).
- **Modelos C4**: Detalhamento da arquitetura em níveis: Contexto, Contêineres, Componentes, Código.

### 3.3. Stack Tecnológica

- **Linguagens de Programação**: Justificativa para a escolha de linguagens específicas.
- **Frameworks e Bibliotecas**: Frameworks e bibliotecas a serem utilizados.
- **Ferramentas de Desenvolvimento e Gestão de Projeto**: Ferramentas para desenvolvimento e gestão do projeto.
  ... qualquer outra informação referente a stack tecnológica ...

### 3.4. Considerações de Segurança

Análise de possíveis questões de segurança e como mitigá-las.

## 4. Próximos Passos

Descrição dos passos seguintes após a conclusão do documento, com uma visão geral do cronograma para Portfólio I e II.

## 5. Referências

Listagem de todas as fontes de pesquisa, frameworks, bibliotecas e ferramentas que serão utilizadas.

## 6. Apêndices (Opcionais)

Informações complementares, dados de suporte ou discussões detalhadas fora do corpo principal.
## 7. Avaliações de Professores

Adicionar três páginas no final do RFC para que os Professores escolhidos possam fazer suas considerações e assinatura:
- Considerações Professor/a:
- Considerações Professor/a:
- Considerações Professor/a:
