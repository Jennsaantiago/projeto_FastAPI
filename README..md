# Desenvolvendo sua Primeira API com FastAPI

Este repositório contém o código e os recursos necessários para desenvolver sua primeira API utilizando o FastAPI, um framework moderno e de alto desempenho para a criação de APIs com Python 3.7+.

## Índice

- [Descrição](#descrição)
- [Requisitos](#requisitos)
- [Instalação](#instalação)
- [Como Executar](#como-executar)
- [Rotas da API](#rotas-da-api)
- [Estrutura do Projeto](#estrutura-do-projeto)
- [Contribuição](#contribuição)
- [Licença](#licença)

## Descrição

Este projeto serve como um guia introdutório para a criação de APIs com o FastAPI. Nele, você aprenderá a configurar seu ambiente, definir rotas, manipular dados e implementar funcionalidades básicas em uma API RESTful.

## Requisitos

- Python 3.14 ou superior
- pip (gerenciador de pacotes do Python)

## Instalação

1. Clone este repositório para sua máquina local:
    ```bash
    git clone https://github.com/seu-usuario/seu-repositorio.git
    cd seu-repositorio
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

## Rotas da API

### `GET /`
- Descrição: Retorna uma mensagem de boas-vindas.
- Resposta:
    ```json
    {
        "message": "Bem-vindo à sua primeira API com FastAPI!"
    }
    ```

### `GET /items/{item_id}`
- Descrição: Retorna os detalhes de um item específico.
- Parâmetros:
    - `item_id`: ID do item a ser retornado.
- Resposta:
    ```json
    {
        "item_id": 1,
        "name": "Item exemplo",
        "description": "Esta é a descrição do item exemplo."
    }
    ```

## Estrutura do Projeto

```
.
├── app
│   ├── __init__.py
│   ├── main.py
│   ├── routers
│   │   └── items.py
│   └── models.py
├── venv
├── requirements.txt
└── README.md
```

- `app/`: Diretório principal do aplicativo.
- `app/main.py`: Arquivo principal onde a aplicação FastAPI é instanciada.
- `app/routers/`: Diretório para os arquivos de rotas.
- `app/models.py`: Arquivo para definição dos modelos de dados.
- `requirements.txt`: Arquivo que contém as dependências do projeto.

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir uma issue ou enviar um pull request.

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).
