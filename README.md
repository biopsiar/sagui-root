<br />
<p align="center">
  <a href="https://github.com/biopsiar/sagui-root">
    <img src="https://raw.githubusercontent.com/biopsiar/biopsiar.github.io/master/img/icons/android-chrome-192x192.png" alt="Logo" width="160">
  </a>
    <br />
    <h3 align="center">
        <strong>SAGUI</strong>
    </h3>
  <p align="center">
    <strong>S</strong>istema de <strong>A</strong>valiação de <strong>G</strong>astos P<strong>ú</strong>bl<strong>i</strong>cos
    <br />
    <h2 align="center">
        <a href="https://biopsiar.github.io/"> Demo <strong>mockup</strong></a>
        Atenção: a versão mockup não é totalmente funcional
    </h2>
    <br />
  </p>
</p>

# ⚠ Aviso
**Certifique-se que essa é a versão mais recente da documentação**  
  
Você pode encontrar a documentação atualizada em: https://github.com/biopsiar/sagui-root

# ℹ Intro
O SAGUI é uma Progressive Web App cuja interação baseia-se no mecanismo de deslizar cartões (swiping app). Nossa stack é composta por Mongo + Flask no back-end para fornecer uma API RESTful e Vue.js + Tailwind.css no front-end para permitir a experiência fluida de uma Single Page Application. O levantamento da aplicação é orquestrado através de uma arquitetura de microserviços com Docker + Docker Compose. Nginx gerencia operações de proxy e Gunicorn fornece o serviço HTTP da API.

# ⚙ Instalação:
0. **Antes de prosseguir, certifique-se de que possui o Docker e Docker Compose instalados:**

    * https://docs.docker.com/compose/install/

1. **Clone esse repositório**
    ```
    maratonista@hackfest:~$ git clone https://github.com/biopsiar/sagui-root.git
    ```

2. **Entre na pasta do repositório clonado**
    ```
    maratonista@hackfest:~$ cd sagui-root
    ```

3. **Dentro dela, clone o repositório `sagui-app` (front-end)**
    ```
    maratonista@hackfest:~/sagui-root$ git clone https://github.com/biopsiar/sagui-app.git
    ```

4. **Clone também o repositório `sagui-api` (back-end)**
    ```
    maratonista@hackfest:~/sagui-root$ git clone https://github.com/biopsiar/sagui-api.git
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

# 🛠 Para desenvolvimento

1. **Abra o terminal na raiz do projeto (sagui-root) e rode o comando:**
    ```
    maratonista@hackfest:~/sagui-root$ docker-compose up -d
    ```
    Esse procedimento levantará os containers e configurações necessárias para rodar a aplicação em modo de *desenvolvimento*. Ou seja, funcionalidades como hot reloading estarão ativas. Você poderá acessar a aplicação no endereço `localhost`. Detalhes das configurações podem ser encontrados no arquivo `docker-compose.yml`.


# 🏭 Para produção

1. **Abra o terminal na raiz do projeto (sagui-root) e rode o comando:**
    ```
    maratonista@hackfest:~/sagui-root$ docker-compose -f docker-compose.prod.yml up -d
    ```
    Esse procedimento levantará os containers e configurações necessárias para rodar a aplicação em modo de *produção*. Qualquer alteração feita nos arquivos da aplicação nesse modo só propagará ao reiniciar os serviços. Você poderá acessar a aplicação no endereço `localhost`. Detalhes das configurações podem ser encontrados no arquivo `docker-compose.prod.yml`.
  

# 🛑 Para parar os serviços

1. **Abra o terminal na raíz do projeto (sagui-root) e rode o comando:**
    ```
    maratonista@hackfest:~/sagui-root$ docker-compose down
    ```

# :tada: **Happy coding**