# Instalação
# <img src="https://avatars0.githubusercontent.com/u/5429470?s=200&v=4" height="38"/> Project setup:
0. **Antes de prosseguir, certifique-se de que possui o Docker e Docker Compose instalados:**

    * https://docs.docker.com/compose/install/

1. **Clone esse repositório**
    ```
    git clone https://github.com/biopsiar/sagui-root.git
    ```

2. **Entre na pasta do repositório clonado**
    ```
    cd sagui-root
    ```

3. **Dentro dela, clone o repositório `sagui-app` (front-end)**
    ```
    git clone https://github.com/biopsiar/sagui-app.git
    ```

4. **Clone também o repositório `sagui-api` (back-end)**
    ```
    git clone https://github.com/biopsiar/sagui-api.git
    ```

5. **Sua pasta `sagui-root` deve estar dessa maneira:**
    ```bash
    └──📁 sagui-root
        ├──📁 nginx
        ├──📁 sagui-api
        ├──📁 sagui-app
        ├──── ...
        └──📄 docker-compose.yml
    ```

# Para desenvolvimento

1. **Abra o terminal na raíz do projeto (sagui-root) e rode o comando:**
    ```
    maratonista@hackfest:~/sagui-root$ docker-compose up -d
    ```
    Esse procedimento levantará os containers e configurações necessárias para rodar a aplicação em modo de *desenvolvimento*. Ou seja, funcionalidades como hot reloading estarão ativas. Você poderá acessar a aplicação no endereço `localhost`. Detalhes das configurações podem ser encontrados no arquivo `docker-compose.yml`.


# Para produção

1. **Abra o terminal na raíz do projeto (sagui-root) e rode o comando:**
    ```
    maratonista@hackfest:~/sagui-root$ docker-compose -f docker-compose.prod.yml up -d
    ```
    Esse procedimento levantará os containers e configurações necessárias para rodar a aplicação em modo de *produção*. Qualquer alteração feita nos arquivos da aplicação nesse modo só propagará ao reiniciar os serviços. Você poderá acessar a aplicação no endereço `localhost`. Detalhes das configurações podem ser encontrados no arquivo `docker-compose.prod.yml`.
  

# Para parar os serviços

1. **Abra o terminal na raíz do projeto (sagui-root) e rode o comando:**
    ```
    maratonista@hackfest:~/sagui-root$ docker-compose down
    ```

# :tada: **Happy coding**