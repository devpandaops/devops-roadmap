## DEVOPS ROADMAP 2022

## Roteiro

#### Ser fundamentalmente forte nas tecnologias de rede
Compreender os conceitos como HTTP/2, QUIC ou HTTP3, protocolos Layer 4 e Layer 7, mTLS, Proxies, DNS, BGP, como funciona o balanceamento de carga, Tabelas IP, o funcionamento da Internet, endereços e esquemas IP e por último a Rede Projeto. Achei o blog da Julia Evans muito útil e meu local de referência quando preciso entender as coisas de uma maneira simples. Ela cobriu uma ampla variedade de tópicos em seus posts e zines.
Domine os fundamentos do sistema operacional, principalmente o Linux
Como a maioria dos sistemas (VMs, Containers, etc) roda Linux, é importante saber de cima para baixo. Aprenda programação, interface systemd, sistema init, cgroups e namespaces, ajuste de desempenho e domine os utilitários de linha de comando — awk, sed, jq , yq, curl, ssh, openssl etc.

#### CI/CD
Se você ainda gosta de Jenkins, tudo bem. Mas, o mundo mudou para pipelines nativos da nuvem. Conceitualmente não mudou muito neste espaço, mas você pode olhar para Github Actions, Tekton etc. Como fazer lançamentos melhor? Entenda várias estratégias de implantação, como azul-verde e canário.
Conteinerização e virtualização
Além do popular tempo de execução do Docker, experimente containerd, podman etc e saiba como conteinerizar aplicativos, como implementar a segurança do contêiner , como executar e orquestrar VMs no Kubernetes, consulte o projeto KubeVirt.

#### Orquestração de contêiner
O Kubernetes agora é um padrão de fato para a execução de contêineres. Há muito conteúdo na Internet para aprender Kubernetes. Concentre-se nas melhores práticas de configuração, design de aplicativos, segurança e agendamento. A configuração de um cluster está ficando trivial agora, mas as coisas operacionais do segundo dia, como configuração, monitoramento, registro, CI/CD, como dimensionar o cluster, otimização de custos e segurança são algumas perguntas que as pessoas podem esperar de você.

#### Observabilidade em escala
A maioria dos engenheiros conhece a pilha Prometheus Grafana ou similar. A tendência sugere que muitas organizações estão consolidando seus clusters e observabilidade do Kubernetes, tanto do ponto de vista de desempenho quanto de custo, isso ajuda. Aprenda a configuração e as arquiteturas avançadas do Prometheus e como escalá-las. Analise tecnologias como Thanos, Cortex, VictoriaMetrics, Datadog e Loki. Ferramentas de perfilamento contínuo, como Parca, periscópio, hypertrace e rastreamento distribuído com telemetria aberta. As malhas de serviço, como o Istio, são ingredientes populares em receitas nativas da nuvem.

#### Equipe de plataforma como uma equipe de produto
A função da equipe de plataforma está se tornando mais parecida com uma equipe de produto centralizada que se concentra em seus clientes de plataforma interna, como desenvolvedores e testadores. O objetivo é melhorar as formas de trabalhar e trazer alguma ordem às equipes. Tente improvisar sobre os problemas que o desenvolvedor e a equipe de controle de qualidade enfrentam. Você é o facilitador para outras equipes, em vez de assumir todo o trabalho em uma equipe central, treine a equipe de desenvolvimento para assumir responsabilidades típicas de DevOps. Dessa forma, você pode escalar e não se queimar muito.

[ add imagem aqui ]

#### Segurança
Em muitas organizações pequenas, a segurança era um cidadão de segunda classe. Os recursos do produto receberam mais prioridade. Mas, devido aos crescentes ataques sofisticados e a vários requisitos de conformidade rigorosos, as empresas estão se adaptando às estratégias de segurança shift-left. Criptografia de ponta a ponta, RBAC forte, políticas de IAM, governança e auditoria, implementação de benchmarks como NIST, CIS, ISO27001 são comuns. Segurança de contêiner, política como código, governança de nuvem e segurança da cadeia de suprimentos são tópicos importantes.

#### Programação
A função de DevOps ou SRE agora está levando as preocupações transversais dos desenvolvedores e criando ferramentas que podem ajudar a melhorar sua produtividade enquanto impõem os padrões. Uma prática e habilidade de engenharia de software de boa qualidade são necessárias para criar os componentes de plataforma de alta qualidade.

Eu não posso dar estresse suficiente para isso. As boas organizações procuram uma boa experiência de programação em engenheiros de plataforma. É importante também na engenharia de confiabilidade do site, onde você precisa ser fluente em programação, capaz de ler, entender e depurar o código escrito por outras pessoas e, se necessário, corrigi-lo.

Python e Golang são os mais populares. Minha sugestão é Golang devido a recursos como forte simultaneidade, verificação estrita de tipos, adoção em várias organizações, cadeia de ferramentas e como muitos projetos importantes são construídos usando Golang, faz sentido aprender isso em Python.

Algumas coisas simples que você pode tentar:

- Escreva uma CLI em sua linguagem de programação.

- Aprenda a escrever uma API REST e interagir com bancos de dados

- Paralelismo e Simultaneidade

#### Infraestrutura como código
Terraform é um padrão nos projetos. Depois de entender o conceito, é fácil se adaptar a qualquer outra ferramenta, pois a maioria delas é baseada em DSL.

#### Nuvem
A maior parte da nuvem funciona da mesma maneira. Portanto, se você conhece bem uma nuvem, pode trabalhar facilmente com outros provedores de nuvem. Concentre-se em como você pode projetar aplicativos usando componentes nativos da nuvem de maneira altamente disponível, resiliente, segura e econômica.

#### Escrita técnica
Você pode estar se perguntando por que estou falando sobre redação técnica ao discutir DevOps. Muitas pessoas não dão atenção suficiente a isso, mas é super importante na forma como você se comunica e trabalha com outras equipes. O futuro do trabalho é remoto e e-mails, slack/equipes, chats são os principais canais para conversar e transmitir ideias para outras pessoas.
Regularmente, você pode estar criando documentos como runbooks, postmortems, RFCs, registros de decisão de arquitetura e documentos de design de software, para citar alguns. Um documento claro e fácil de entender faz maravilhas. Ele pode ajudá-lo a economizar seu tempo e o do leitor e melhorar a produtividade geral. Sugiro que leia este artigo .

#### Engenharia de confiabilidade do site
A fronteira entre DevOps e SRE está ficando tênue. Em algumas organizações, a mesma pessoa pode estar desempenhando as duas funções. Entenda os conceitos por trás de SLI, SLO e orçamentos de erro e práticas de SRE. Cada organização faz isso de forma diferente, então não recomendo copiar e colar a cultura de outra pessoa em sua equipe. Consulte a cultura do Google SRE .

#### Conclusão
Pessoalmente, estou animado em seguir este ano. Esta não é uma lista definitiva, pois continua mudando com o tempo.

- Service Mesh — Istio, Cilium Sidecarless mesh, Tetrate e Solo's Gloo mesh.

- Como melhorar a produtividade do desenvolvedor? É uma mistura de cultura, automação e ferramentas.

- Plataformas SRE — favo de mel , Last9.

- DevPortals — novamente ligados ao motivo de melhorar a produtividade e preencher a lacuna de conhecimento.

- Observabilidade — tecnologias como telemetria aberta, hypertrace, Thanos , VictoriaMetrics, Vector.

- Segurança — segurança da cadeia de suprimentos, assinatura de código, reforço da segurança na nuvem.

- Golang — melhorando as habilidades atuais.

- Computação sem servidor e arquiteturas orientadas a eventos

- Web3 — entendendo o cenário relacionado a DevOps e infraestrutura

