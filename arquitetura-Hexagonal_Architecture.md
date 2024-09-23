FUNCIONAMENTO

A ideia central da Hexagonal Architecture é que o núcleo do sistema seja independente de fatores externos, como frameworks ou bancos de dados, e interaja com
eles através de "portas" e "adaptadores":
-Núcleo (Domínio de Negócio): Representa a lógica de negócios, que deve ser pura, sem referências diretas a tecnologias externas.
-Portas: Definem interfaces para as funcionalidades do núcleo, permitindo que diferentes adaptadores (tecnologias externas) se conectem a ele.
-Adaptadores: São implementações concretas que utilizam as portas para conectar tecnologias externas ao núcleo. Podem ser adaptadores para interface de usuário
(UI), banco de dados, sistemas externos, etc.

COMO SURGIU

A Hexagonal Architecure surgiu porque Alistair Cockburn percebeu que, com o tempo, camadas como a de apresentação ou de persistência acabavam contaminando o
núcleo da aplicação, dificultando a manutenção e os testes. Em resposta a isso, AListair criou a Hexagonal Architecture em 2005, com o objetivo de desacoplar 
o núcleo da aplicação das implementações técnicas para que o software possa ser facilmente adaptado ou modificado sem grandes impactos.

PROPÓSITO

O principal propósito da Hexagonal Architecture é promover o isolamento do domínio de negócios, tornando a aplicação:
-Mais modular: facilita a substituição de partes do sistema, como mudar de um banco de dados para outro ou de uma interface de usuário para outra.
-Fácil de testar: como o núcleo é independente, ele pode ser testado isoladamente, sem a necessidade de bancos de dados ou serviços externos.
-Facilmente extensível: é possível adicionar novos adaptadores (novas tecnologias ou integrações) sem alterar o núcleo da aplicação.

PROBLEMAS RESOLVIDOS PELA ARQUITETURA

-Dependência excessiva de infraestrutura: Evita que o núcleo da aplicação fique acoplado a frameworks ou tecnologias específicas.
-Testabilidade: Ao isolar a lógica de negócios, fica mais fácil testar o domínio sem precisar de dependências externas, como bancos de dados ou APIs.
-Facilidade de troca de componentes: Você pode trocar bancos de dados, frameworks de UI ou outras dependências externas sem tocar no núcleo da aplicação.
-Manutenção simplificada: A arquitetura modular facilita a localização e correção de bugs, além de permitir modificações sem impacto em todo o sistema.

PROBLEMAS QUE AINDA EXISTEM NESSE MODELO

-Complexidade adicional: A introdução de portas e adaptadores pode aumentar a complexidade do código, especialmente em sistemas simples, onde essa separação -pode parecer excessiva.
-Curva de aprendizado: Para desenvolvedores menos experientes, pode ser difícil entender e implementar corretamente a arquitetura hexagonal.
-Overhead na separação: Em alguns casos, a separação excessiva pode gerar mais código, criando uma sobrecarga de manutenção e estrutura desnecessária para aplicações menores.
-Implementações inconsistentes: Como a arquitetura hexagonal não possui um conjunto rígido de regras, diferentes equipes podem interpretá-la de formas variadas, o que pode resultar em inconsistências.
