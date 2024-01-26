# Arquitetura MiniCore

MiniCore: Esta arquitetura foi concebida com o objetivo de facilitar as responsabilidades em diferentes camadas, proporcionando uma abordagem que simplifica a manutenção, promove a estabilidade e aprimora a escalabilidade do código. Cada camada possui um propósito distinto, e as dependências são estruturadas de maneira a evitar fortes acoplamentos entre a lógica de negócios e a implementação técnica. Isso resulta em um sistema flexível e facilmente evolutivo.

<br>

A Arquitetura MiniCore é estruturada em quatro camadas distintas:

## Public
Onde encontramos todas as páginas e subpáginas do aplicativo.

## Interactor
Responsável pela execução das regras de negócios.

## Data
Encarrega-se da comunicação e transformação dos dados.

## Core
Desempenha o papel crucial de compartilhar classes ou arquivos essenciais em toda a aplicação, promovendo uma base robusta e coesa para o desenvolvimento.

<img src="mini_core.png" width="512" alt="Achitecture diagram"/>   

## Public
Na camada Public, encontram-se as páginas e subpáginas do aplicativo, sendo responsável pela apresentação visual e interativa.

## Interactor
Na camada Interactor, assume-se a responsabilidade pela execução das regras de negócios. Nela, estão presentes elementos essenciais como atoms, actions, dtos, models, contratos do repositório e serviços.

- Atoms: Atom refere-se a um estado que possui reatividade própria, contribuindo para a dinâmica do objeto.

- Actions: Actions têm o propósito de executar as regras de negócio, promovendo a implementação prática das operações necessárias.

- DTO: Ou Data Transfer Object, é um padrão de design usado para transferir dados entre camadas, assegurando uma comunicação eficiente.

- Models: Models representam a essência das regras de negócio, incorporando funcionalidades como fromMap e toJson para facilitar a serialização.

- Contratos: Nessa seção, incluímos interfaces do repositório e serviços, delineando claramente os compromissos necessários.

## Data
A camada Data assume a responsabilidade de interagir tanto com fontes externas (APIs) quanto internas (Banco de dados locais).

- Repository: O padrão Repository proporciona uma abstração entre a lógica de negócios e o acesso aos dados, simplificando a gestão e manipulação desses dados.

- Service: O padrão Service, amplamente utilizado em arquiteturas de software, encapsula a lógica de negócios para promover modularidade, reutilização e facilidade de manutenção.

## Core
Na camada Core, encontram-se dados globais e reutilizáveis fornecidos para todas as camadas da aplicação, incluindo como exemplo: temas, widgets, design system e dados compartilhados. Essa camada é fundamental para manter a coesão e consistência em toda a aplicação.

## Benefícios da Utilização da Arquitetura MiniCore:

- #### Facilidade de Entendimento: 
    Proporciona uma estrutura clara e intuitiva, facilitando a compreensão do código para desenvolvedores.

- #### Manutenibilidade:
    A divisão em camadas e a clareza das responsabilidades tornam o código mais fácil de manter e atualizar.

- #### Escalabilidade de Código:
    A arquitetura é projetada para lidar com o crescimento da aplicação, garantindo que ela possa escalar de maneira eficaz.

- #### Acesso Fácil a Variáveis e Métodos Globais:
    Facilita o acesso a variáveis e métodos globais, promovendo uma comunicação eficiente entre as diferentes partes do sistema.

- #### Facilita Testes (Sem a Necessidade de Mockar os Atoms):
    Simplifica a realização de testes, eliminando a necessidade de simular ou simbolizar (mockar) os Atoms, tornando o processo de teste mais eficiente e menos complexo.

<br>

Ao adotar a arquitetura MiniCore, os desenvolvedores ganham um desenvolvimento de sistemas mais robustos, eficientes e de fácil manutenção, promovendo uma experiência de desenvolvimento mais positiva e sustentável.