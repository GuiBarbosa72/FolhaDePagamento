# Sistema de Folha de Pagamento

Um sistema desenvolvido em Programação Orientada a Objetos para automação dos processos de gestão de funcionários, apuração de vencimentos e descontos salariais e emissão de holerites.

## Descrição do Projeto

O objetivo principal desta aplicação é oferecer uma estrutura clara e eficiente para o gerenciamento de pessoal de uma empresa. O sistema organiza as informações de cada colaborador, registra suas horas trabalhadas ou tipo de contrato e calcula automaticamente o salário bruto e líquido. A lógica aplicada efetua as deduções obrigatórias de impostos de acordo com as tabelas vigentes, contabiliza adicionais e gera os relatórios financeiros da folha de pagamento de forma individual ou consolidada.

## Arquitetura e Conceitos Aplicados

A solução foi estruturada aplicando os pilares da Programação Orientada a Objetos para garantir facilidade de manutenção, extensibilidade e reutilização de código.

A abstração e a herança foram utilizadas na construção da hierarquia de colaboradores, onde uma classe principal define os atributos e comportamentos fundamentais e subclasses lidam com especificidades de cada modalidade contratual.

O encapsulamento protege informações sensíveis como dados pessoais e valores monetários, restringindo o acesso direto a atributos por meio de métodos de acesso e modificação devidamente controlados.

O polimorfismo é empregado na rotina de cálculo salarial, permitindo que cada tipo de contrato sobrescreva a lógica de cálculo para aplicar suas próprias regras de adicionais e descontos sem alterar a interface comum do sistema.

## Estrutura do Repositório

```text
FolhaDePagamento/
├── src/
│   ├── models/
│   │   ├── Funcionario.java
│   │   ├── FuncionarioCLT.java
│   │   ├── FuncionarioPJ.java
│   │   └── Holerite.java
│   └── services/
│       ├── CalculadoraImpostos.java
│       └── FolhaPagamentoService.java
└── README.md
