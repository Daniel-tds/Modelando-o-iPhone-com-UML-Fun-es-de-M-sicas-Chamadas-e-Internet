# Modelando o iPhone com UML: Funções de Músicas, Chamadas e Internet

Este projeto é uma implementação em Java/UML que simula as funcionalidades do iPhone com base no vídeo de lançamento do iPhone, modeladas com UML, contemplando:

- Reprodutor Musical (tocar, pausar, selecionar música)
- Aparelho Telefônico (ligar, atender, iniciar correio de voz)
- Navegador na Internet (exibir página, adicionar nova aba, atualizar página)

## Diagrama UML

O projeto foi modelado utilizando interfaces para representar cada funcionalidade, e a classe `Iphone` implementa essas interfaces, conforme o diagrama UML a seguir:

```mermaid
classDiagram
    direction TB

    class ReprodutorMusical {
        +tocar()
        +pausar()
        +selecionarMusica(musica: String)
    }

    class AparelhoTelefonico {
        +ligar(numero: String)
        +atender()
        +iniciarCorreioVoz()
    }

    class NavegadorInternet {
        +exibirPagina(url: String)
        +adicionarNovaAba()
        +atualizarPagina()
    }

    class Iphone {
    }

    Iphone --> ReprodutorMusical
    Iphone --> AparelhoTelefonico
    Iphone --> NavegadorInternet
