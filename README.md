'''mermaid
classDiagram
    class Usuario {
        +String name
    }

    class Conta {
        +String number
        +String agency
        +Float balance
    }

    class Funcionalidade {
        +String icon
        +String description
    }

    class Cartao {
        +String number
        +Float limit
    }

    class Noticia {
        +String icon
        +String description
    }

    Usuario "1" --> "1" Conta
    Usuario "1" --> "1..*" Funcionalidade
    Usuario "1" --> "1" Cartao
    Usuario "1" --> "0..*" Noticia

    '''
