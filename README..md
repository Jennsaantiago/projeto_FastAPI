# Desenvolvendo sua Primeira API com FastAPI

Este repositório contém o código e os recursos necessários para desenvolver minha primeira API utilizando o FastAPI, um framework moderno e de alto desempenho para a criação de APIs com Python 3.14+.

## Descrição

Este projeto serve como um guia introdutório para a criação de APIs com o FastAPI, no tema de Crossfit. Nele, você aprenderá a configurar seu ambiente, definir rotas, manipular dados e implementar funcionalidades básicas em uma API RESTful.

## Requisitos

- Python 3.14 ou superior
- pip (gerenciador de pacotes do Python)

## Instalação

1. Clone este repositório para sua máquina local:
    ```bash
    git clone https://github.com/Jennsaantiago/projeto_FastAPI
    cd projeto_FastAPI
    ```

2. Crie um ambiente virtual:
    ```bash
    python -m venv venv
    ```

3. Ative o ambiente virtual:

    - No Windows:
        ```bash
        venv\Scripts\activate
        ```
    - No macOS/Linux:
        ```bash
        source venv/bin/activate
        ```

4. Instale as dependências:
    ```bash
    pip install -r requirements.txt
    ```

## Como Executar

1. Execute o servidor FastAPI:
    ```bash
    uvicorn main:app --reload
    ```

2. Acesse a documentação interativa da API no seu navegador:
    ``` 
    http://127.0.0.1:8000/docs 
    ```

3. Acesse a documentação alternativa da API (Redoc):
    ``` 
    http://127.0.0.1:8000/redoc 
    ```
    
Para subir o banco de dados, caso não tenha o [docker-compose](https://docs.docker.com/compose/install/linux/) instalado, faça a instalação e logo em seguida, execute:

```bash
make run-docker
```
Para criar uma migration nova, execute:

```bash
make create-migrations d="nome_da_migration"
```

Para criar o banco de dados, execute:

```bash
make run-migrations
```

## API

Para subir a API, execute:
```bash
make run
```
e acesse: http://127.0.0.1:8000/docs


## Desafio Final

- adicionar query parameters nos endpoints
    - atleta
        - nome
        - cpf
- customizar response de retorno de endpoints
    - get all
        - atleta
            - nome
            - centro_treinamento
            - categoria
- Manipular exceção de integridade dos dados em cada módulo/tabela
    - sqlalchemy.exc.IntegrityError e devolver a seguinte mensagem: “Já existe um atleta cadastrado com o cpf: x”
    - status_code: 303
- Adicionar paginação utilizando a lib: fastapi-pagination
    - limit e offset

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir uma issue ou enviar um pull request.

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).
