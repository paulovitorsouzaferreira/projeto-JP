erDiagram
    CLIENTE {
        int ID_CLIENTE PK
        string NOME
        date DATA_NASCIMENTO
        string FIADOR
        string CONTATO
        string DOCUMENTO
        string TIPO_DOCUMENTO
        string OBS
    }
    AGENDAMENTO {
        int ID_AGENDAMENTO PK
        int ID_CLIENTE FK
        date CHECK_IN
        date CHECK_OUT
        string TIPO_QUARTO
        string OBS
    }
    FUNCIONARIO {
        int ID_FUNCIONARIO PK
        string USUARIO
        string SENHA
    }
    PRODUTO {
        int ID_PRODUTO PK
        string NOME
        decimal VALOR
    }
    SERVICO {
        int ID_SERVICO PK
        string TIPO
        decimal VALOR
    }
    CLIENTE ||--o{ AGENDAMENTO : "realiza"
    AGENDAMENTO ||--o{ PRODUTO : "consome"
    AGENDAMENTO ||--o{ SERVICO : "utiliza"
