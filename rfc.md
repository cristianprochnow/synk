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

- **Contexto**: Essa aplicação visa resolver problemas de gargalo em uma comunicação digital. Hoje em dia as pessoas estão totalmente presente em redes sociais ou outros meios de comunicação, sendo assim, é onde empresas também querem estar presente constantemente. Para esse processo, ter como objetivo a interação nas redes sociais é extremamente relevante, estando sempre perto de seu público. Além disso, a facilidade proporcionada por ter uma ferramenta que automatiza tarefas maçantes é de grande valia, principalmente no dia a dia corporativo ao qual tudo passa muito rápido. Sendo assim, é para isso que Synk surge, para proporcionar facilidade onde é tipicamente tudo baseado na escrita manual de comunicados e publicações.
- **Justificativa**: A existência é justificada pelo tempo que vai ser preservado daqueles que realizam processos manuais e também em proporcionar facilidade para até mesmo que não tem tempo consiga realizar a publicação desejada. Essas publicações se referem à qualquer *post* em qualquer rede social disponível como integração na aplicação. Seja para um comunicado nas redes sociais, um *post* comercial no LinkedIn, um resumo da nova atualização que ocorreu no sistema ou produto que está sendo tratado por meio do Slack ou Teams, e assim segue. Nos dias atuais o tempo sempre parece que passa tão rápido, portanto fica evidente que qualquer forma de minimizar o gasto dele se torna um grande atrativo para qualquer uso.
- **Objetivos**: Synk tem como objetivo ser uma plataforma integrada com diversas plataformas de comunicação e divulgação, oferecendo então uma interface prática para que o usuário possa salvar templates e rapidamente ajustá-los para publicação, tudo isso em poucos cliques e otimizando o que seja estático. O objetivo dessa aplicação não é ser um CRM e nem se tornar um, e sim resolver os problemas que ficam na base da pirâmide da produtividade e aos quais geralmente são gastos tanto tempo por serem considerados triviais - mas ainda sim volumétricos, gastando tempo.

## 2. Descrição do Projeto

- **Tema do Projeto**: Synk é uma ferramenta para gerenciamento de templates para publicações em diversas redes sociais e meios de comunicação. Então por meio dessa aplicação, poderá gerenciar templates, customizar conforme deseja o texto, importar de alguma fonte, e após isso, publicar para qualquer uma das plataformas disponíveis para integração - desde que esteja configurada.
- **Problemas a Resolver**: Um dos grandes problemas de ter que inserir o mesmo conteúdo em várias redes sociais e diversas fontes de comunicação é ter que ter o meso texto, em vários formatos. Ou, também, ter que entrar de aplicação em aplicação copiando e colando o texto para que fique todas as redes no mesmo formato. Sendo assim, Synk chega para resolver exatamente esse ponto, ao qual pode deixar pré-configurado diversos templates, pré-determinados para determinadas redes sociais para diferentes contextos. Então, ao invés de bolar o texto e ainda ter que selecionar onde publicar, como publicar e assim por diante, Synk já deixa tudo isso organizado e unificado para facilitar a vida.
- **Limitações**: Aplicações CRM fazem algo parecido e até mais avançado, ao qual além de publicar, ainda retorna métricas de tudo aquilo que foi colocado no ar. Contudo, Synk não tem isso como objetivo, e o foco principal é facilitar o trabalho maçante de organizar tudo e categorizar o conteúdo de forma ideal. Portanto, o objetivo é a parte prática de criar o conteúdo e publicar, facilitando então a parte que mais gasta tempo e geralmente é negligenciada por ser considerada por muitos "trivial".

## 3. Especificação Técnica

O projeto tem como objetivo o gerenciamento de templates que são relacionados a cada usuário. O uso desses templates poderá ser feito para publicação em redes sociais que a aplicação tiver integração. Cada uma dessas integrações vão necessitar das configurações específicas, contendo então os dados de acesso para cada uma que for desejada. Além disso, há também a funcionalidade de importar conteúdo de algum _post_ específico, para que o usuário possa transformar qualquer conteúdo em template. Partindo desse pressuposto, temos então os alicerces de:

* Gerenciamento de usuário
* Gerenciamento de templates
* Gerenciamento de perfis de integração
* Integração com redes sociais para realizar _posts_
* Importação de conteúdo por meio de link
* Interface avançada para edição de texto

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

#### 3.2.1. Visão inicia

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
