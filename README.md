```mermaid
classDiagram
    class Pagina {
        - conteudoData: String
        - conteudoExercicio: List
        - conteudoConcluidos: List
        + avancar()
        + voltar()
        + inicio()
    }

    class Conteudo {
        - data: String
        - exercicioDoDia: String
    }
    Conteudo --|> Pagina

    class ListaDeExercicios {
        - exercicio: String
        - estadoDoexercicio: Boolean
        + iniciarExercicio()
        + verListaDeExercicios()
        + verListaDeExerciciosConcluidos()
    }
    ListaDeExercicios --|> Pagina

    class Exercicio {
        - equipamento: String
        - repeticoes: int
        - diaDaSemana: String
    }
    Exercicio --|> ListaDeExercicios
