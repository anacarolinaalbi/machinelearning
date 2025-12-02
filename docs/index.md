# Template de Entrega

Esse material foi produzido inicialmente durante a matéria de Machine Learning ministrada por Humberto Sandmman como entrega obrigatório do segundo semestre de 2025.


# PORTIFÓLIO

Olá, seja bem vindo.

Meu nome é Ana Carolina Albi Pereira. As pessoas costumam me chamar de Ana, Carol ou Albi. Nasci no dia 29 de dezembro de 2004. Desde então, fui uma criança bem comuncativa, curiosa e feliz. Conheci a tecnologia ainda na escola, tendo contato com programas como sketch, pacote office e adobe, programação em si de arduíno e noções de projetos de inovação. No final do ensino médio, trabalhei por alguns meses em uma gráfica na Vila Olímpia, onde pude lidar com organização de processos, atendimento ao cliente, faturamento e orçamento, além do que participei da implantação de um novo produto/serviço oferecido pela empresa, que posteriormente, acabou por não passar de um teste. No cursinho BNE, conheci as pessoas que estudariam comigo no Insper, faculdade a qual fiquei aproximadamente 2 anos afiliada. Como não sou uma pessoa extremamente técnica, ciência da computação não era "meu número". Hoje, cursando ciência de dados para negócios na ESPM Tech, acredito ter me encoontrada quanto aos pilares que movem minha cabeça e meu coração: tecnologia e comunicação.


???+ info inline end "Edição"

    2025.1



!!! tip "Algorítimos"

    Bloco de notas para registrar o que foi feito e o que falta fazer.

## Entregas

- [x] DECISION TREE - Data 23/02/2025
- [x] KNN
- [x] K-MEAN
- [x] EVALUATION AND METRICS
- [x] DATA PROJECT I
- [x] RANDOM FOREST
- [ ] PYSPARK
- [ ] PAGE RANK
- [x] DATA PROJECT II
- [ ] SUPPORT VECTOR MACHINE

## Diagramas

Use o [Mermaid](https://mermaid.js.org/intro/){:target='_blank'} para criar os diagramas de documentação.

[Mermaid Live Editor](https://mermaid.live/){:target='_blank'}


``` mermaid
flowchart TD
    Deployment:::orange -->|defines| ReplicaSet
    ReplicaSet -->|manages| pod((Pod))
    pod:::red -->|runs| Container
    Deployment -->|scales| pod
    Deployment -->|updates| pod

    Service:::orange -->|exposes| pod

    subgraph  
        ConfigMap:::orange
        Secret:::orange
    end

    ConfigMap --> Deployment
    Secret --> Deployment
    classDef red fill:#f55
    classDef orange fill:#ffa500
```



## Códigos

=== "De um arquivo remoto"

    ``` { .yaml .copy .select linenums='1' title="main.yaml" }
    --8<-- "https://raw.githubusercontent.com/hsandmann/documentation.template/refs/heads/main/.github/workflows/main.yaml"
    ```

=== "Anotações no código"

    ``` { .yaml title="compose.yaml" }
    name: app

        db:
            image: postgres:17
            environment:
                POSTGRES_DB: ${POSTGRES_DB:-projeto} # (1)!
                POSTGRES_USER: ${POSTGRES_USER:-projeto}
                POSTGRES_PASSWORD: ${POSTGRES_PASSWORD:-projeto}
            ports:
                - 5432:5432 #(2)!
    ```

    1.  Caso a variável de ambiente `POSTGRES_DB` não exista ou seja nula - não seja definida no arquivo `.env` - o valor padrão será `projeto`. Vide [documentação](https://docs.docker.com/reference/compose-file/interpolation/){target='_blank'}.

    2. Aqui é feito um túnel da porta 5432 do container do banco de dados para a porta 5432 do host (no caso localhost). Em um ambiente de produção, essa porta não deve ser exposta, pois ninguém de fora do compose deveria acessar o banco de dados diretamente.


## Exemplo de vídeo

Lorem ipsum dolor sit amet

<iframe width="100%" height="470" src="https://www.youtube.com/embed/3574AYQml8w" allowfullscreen></iframe>


## Referências

[Material for MkDocs](https://squidfunk.github.io/mkdocs-material/reference/){:target='_blank'}