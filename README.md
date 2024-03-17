# Domain
- É o négocio da sua empresa ou o assunto do seu projeto

# Core Domain
- É a principal parte de um domain

# Development team
- Programadores

# Domain Experts
- São os expecialistas no négocio
ex:
 estamos criando uma aplicação para auxiliar um escritório de Advocacia, os advogados seria os "Domain Experts"
 sendo capaz de guiar a equipe para desenvolver um bom software tirando dúvidas, definindo regras de processos e termos.

# Linguagem Ubíqua
- Usado para os "Domain Experts" se comunicar de forma clara com o "Development team"
- A "Linguagem ubíqua" é a linguagem da equipe, compartilhada e principalmente entendido por todos
- Durante o projeto ela também vai evoluindo
ex:
 O "Development team" pensa em classes, métodos, componentes, quais objetos criar, qual relacionamento entre eles, heranças, polimorfismo etc.
 Já os "Domain Experts" não sabem nada disso e também sabem muitos termos do assunto do projeto que os "Development team" não sabem.

# Bounded Context 
- Irá delimitar o contexto baseado nas intenções do negócio
- Ela é o limite conceitual, uma vez que todo "Domain" for colocado em um modelo ela pode se torna complexo demais
- Cada "Bounded Context" poderá ter sua "Linguagem ubíqua", abordagem de arquitetura, armazenamento de dados e até sua própia "Development team" 

# Contax Map
- O modelo que vai dar a visão geral do software

# Os principais tipos de relacionamento
- Shared Kernel: 
  Quando vários "Bounded Context" compartilham de um mesmo "Domain". Alterar ele significa que todas as equipes serão afetadas.

- Customer-Suplier Development:
  Quando existe um relacionamento entre cliente e servidor, chamado no "DDD" de "Downstream" e "Upstream" ("upstream" pode ter êxito interdependente da equipe "downstream")

- Conformist:
  O "Bounded Context" "downstream" está conformado que o modelo "upstream" não atende suas necessidades e que as modificações realizadas por ele ("downstream") 
  irá impactar diretamente em seu contexto

- Partner
  São os "Bounded Context" que são parceiros, unidos por uma dependência mútua e deverão trabalhar em conjunto

- Anticorruption Layer
  Nesse relacionamento a equipe "downstream" decide cirar uma camada para protejer o seu contexto das modificações do "upstream" (é muito comun encontrar em sistemas legados)


# Design Estratégico
- É basicamente tudo que foi citado acima
  "É como fazer o rascunho antes de entrar nos detalhes da aplicação" - Vaughn Vemon

# Design Tático
- Diz a respito da implementação e usa o modelo "Domain Model Pattern"
- Possui alguns padrões como por exemplo o "Entities" e o "Value objects" que define os conceitos do domínio
- "Domain Service" que assume responsabilidades que não se encaixam em outros projetos
- "Aggregates" que define fronteiras entre os objetos
- "Factories" e o "Repositories" que lidam com a criação e armazenamento de objetos