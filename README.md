Concessionária – Sistema de Gerenciamento

Este projeto foi desenvolvido com o objetivo de gerenciar as operações de uma concessionária de veículos.
O sistema permite controlar clientes, veículos, vendas, financiamentos, test drives e oferece uma interface simples via console.

É um projeto pensado para demonstrar boas práticas de Engenharia de Software, incluindo modelagem, arquitetura MVC, documentação e organização do código.

Arquitetura do Sistema

O projeto segue o padrão MVC (Model–View–Controller):

Model: Representa as entidades e regras de negócio

View: Interação com o usuário via console

Controller: Processa entradas, coordena lógica e chama os Models

Estrutura:

src/
 ├── Controller/
 ├── Interface/
 ├── Model/
 ├── Util/
 └── View/
Requisitos Funcionais

RF01 — Gerenciar Clientes
O sistema deve permitir cadastrar, consultar, atualizar e listar clientes.

RF02 — Gerenciar Veículos
O sistema deve registrar carros e motos, além de listar e consultar detalhes.

RF03 — Registrar Vendas
O sistema deve permitir registrar uma venda com cliente, veículo e vendedor.

RF04 — Histórico de Vendas do Cliente
O sistema deve apresentar todas as vendas feitas a um cliente.

RF05 — Test Drives
O sistema deve agendar e consultar test drives.

RF06 — Gerenciar Financiamentos
O sistema deve registrar um financiamento associado a uma venda.

RF07 — Menu principal navegável
O sistema deve apresentar um menu com as opções disponíveis.

Requisitos Não Funcionais

RNF01 — Linguagem: Java
RNF02 — Interface: Console (CLI)
RNF03 — Arquitetura: MVC
RNF04 — Persistência em memória (sem banco de dados)
RNF05 — Código legível e orientado a objetos

Casos de Uso
Caso de Uso 01 — Cadastrar Cliente

Ator: Atendente
Fluxo: Inserir nome, CPF, telefone → Cliente é criado e armazenado
Pré-condição: CPF válido
Pós-condição: Cliente fica disponível para vendas e test drives

Caso de Uso 02 — Registrar Venda

Ator: Vendedor
Fluxo: Selecionar cliente → Veículo → Registrar pagamento → Finalizar
Pós-condição: Venda associada ao cliente e veículo marcado como vendido

Caso de Uso 03 — Agendar Test Drive

Ator: Cliente
Fluxo: Informar cliente + veículo + data
Pós-condição: Test drive registrado no sistema

Diagrama de Classes (UML)

<img width="1274" height="1274" alt="mermaid-diagram" src="https://github.com/user-attachments/assets/e7bc5772-0241-4ded-a73d-54045aaa7448" />


Relacionamentos Entre Classes

Agregação: Cliente → Venda (um cliente pode ter várias vendas)

Composição: Venda depende de Cliente + Veículo + Vendedor

Associação: Financiamento → Venda

Como Executar o Projeto

Clone o repositório:

git clone https://github.com/SEU-USUARIO/Concessionaria.git

Entre no diretório:

cd Concessionaria

Compile:

javac src/**/*.java

Execute a classe main (exemplo):

java src.View.MenuPrincipal
Tecnologias Utilizadas

Java

Paradigma Orientado a Objetos

Padrão MVC

UML (documentação)
