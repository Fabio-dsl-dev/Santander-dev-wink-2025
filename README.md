'''mermaid
classDiagram
    class Cliente {
        +String nomeCompleto
        +String dataNascimento
        +Endereco endereco
        +List~ContaBancaria~ contasBancarias
    }

    class Endereco {
        +String rua
        +int numero
        +String cidade
        +String estado
        +String cep
    }

    class ContaBancaria {
        +String numeroConta
        +String tipo
        +double saldo
        +List~Transacao~ transacoes
    }

    class Transacao {
        +String data
        +String descricao
        +double valor
        +String tipoTransacao
    }

    Cliente "1" *-- "1" Endereco
    Cliente "1" *-- "*" ContaBancaria
    ContaBancaria "1" *-- "*" Transacao
    '''
