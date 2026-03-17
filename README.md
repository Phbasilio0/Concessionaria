#Concessionária – Sistema de Gerenciamento

Um projeto completo de Engenharia de Software, estruturado em camadas (MVC) e desenvolvido em Java.

Visão Geral

Este sistema tem como objetivo gerenciar todas as operações de uma concessionária de veículos, oferecendo funcionalidades para:

Cadastro e gerenciamento de Clientes

Administração de Veículos (carros e motos)

Registro e controle de Vendas

Controle de Financiamentos

Agendamento e gerenciamento de Test Drives

O foco principal é simular um ambiente real de uma concessionária, utilizando boas práticas de programação orientada a objetos, organização modular e princípios de engenharia de software.

Arquitetura e Modelagem

O projeto segue uma arquitetura baseada em MVC (Model–View–Controller), promovendo separação de responsabilidades e facilidade de manutenção.

Relações Entre Classes

- Agregação

A classe Cliente mantém um histórico de vendas.

O cliente existe sem a venda, mas a venda sempre referencia um cliente.

- Composição

A classe Venda é composta por Cliente, Vendedor e Veículo.

A venda não existe sem esses elementos.

- Associação

A classe Financiamento está associada diretamente a uma Venda,
indicando dependência direta entre ambas.

 Estrutura do Projeto
src/
 ├── Model/          # Classes de domínio (Cliente, Veículo, Venda, etc.)
 ├── Controller/     # Lógica de controle e regras de negócio
 ├── View/           # Interface textual com o usuário
 ├── Interface/      # Interfaces utilizadas no sistema
 └── Util/           # Utilidades e classes auxiliares
 Como Executar o Projeto

Clone o repositório:

git clone https://github.com/Phbasilio0/Concessionaria.git

Acesse o diretório do projeto:

cd Concessionaria

Compile o projeto:

javac src/**/*.java

Execute a aplicação (classe principal):

java src/View/MenuPrincipal

Interaja com o sistema pelo console.

Habilidades Demonstradas

Este projeto evidencia competências importantes de um Engenheiro de Software:

Programação Orientada a Objetos (POO)

Modelagem UML (agregação, composição e associação)

Arquitetura MVC

Boas práticas de organização de código

Manipulação de dados em estruturas de classes

Simulação de regras de negócio reais

