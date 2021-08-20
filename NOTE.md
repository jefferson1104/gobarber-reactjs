## DEPLOY DE APLICAÇÕES REACTJS

Nesse artigo eu vou explicar como fazer o deploy de uma aplicação feita com ReactJS, no geral aplicações front-ent é muito mais facil de colocar em produção do que back-end, mas nesse tutorial eu vou mostrar 2 alternativas diferentes para fazer deploy, a primeira opção com um nível iniciante e intermediário e a segunda alternativa com um nível mais avançado, estamos falando de realizar um deploy utilizando serviços como netlify, heroku, vercel e etc... e a outra alternativa seria criar um servidor/vps onde vamos fazer o deploy do nosso projeto reactJS.

### Preparando projeto para deploy

Como utilizamos o "Create React App" para criar esse projeto não teremos dificuldade para deixar pronto para deploy, se você observar o package.json vai ver que ja até existe um script para fazer build do projeto.

Porém é necessário que você tenha configurado suas variaveis de ambiente no projeto, nesse projeto do **goBarber** por exemplo temos um serviço de api então criamos um `.env` na raiz do projeto com a variável de ambiente `REACT_APP_API_URL` e utilizamos no `src/services/api.ts`.

![deploy](./assets/deploy/guia-reactjs-deploy-02.png)

![deploy](./assets/deploy/guia-reactjs-deploy-03.png)

> **NOTA**: é necessário que no início do nome de toda variavel que você criar insira o "REACT_APP" seguindo esse modelo "REACT_APP_NOME_DA_VARIAVEL"

### Deploy utilizando o Netlify

O netlify é uma ótima opção para fazer deploy de aplicações ReactJS, sem duvidas é uma plataforma para hospedagem maravilhosa e o melhor de tudo é que ele tem um plano gratuito muito bom, também existem outros serviços como o heroku, vercel e etc...

> **NOTA**: é necessário que você tenha um cadastro no netlify, e que você tenha seu projeto em um repositório no GitHub, GitLab ou Bitbucket.

![deploy](./assets/deploy/guia-reactjs-deploy-01.png)

Após fazer login no netlify, navegue até o menu **Sites** e em seguida clique no botão **New site from Git**.
![deploy](./assets/deploy/guia-reactjs-deploy-04.png)

Escolha uma opção para fazer a integração do seu repositório, nesse caso meu projeto está no **GitHub** entao foi a opção que escolhi.
![deploy](./assets/deploy/guia-reactjs-deploy-05.png)

Procure pelo seu repositório e clique nele.
![deploy](./assets/deploy/guia-reactjs-deploy-06.png)

Agora se você criou seu projeto com o "Create React App" igual fizemos no projeto gobarber você mantem as configurações como mostra nas imagens abaixo, clique no botão **Show advanced**.
![deploy](./assets/deploy/guia-reactjs-deploy-07.png)
![deploy](./assets/deploy/guia-reactjs-deploy-08.png)

Você vai perceber que temos novas opções uma delas é o botão **New variable** vamos clicar nele para inserir nossa variavel de ambiente, em seguida clique no botão **Deploy site**.
![deploy](./assets/deploy/guia-reactjs-deploy-09.png)

Feito os passos anterior você vai parar em uma tela como mostra a imagem abaixo, o processo de deploy da aplicação iniciou.
![deploy](./assets/deploy/guia-reactjs-deploy-10.png)

Com essa opção de deploy no netflify conseguimos utilizar recursos como: funções serveless, CI/CD, previews de pull requests, CDN para arquivos grandes, Analytics, autenticações, utilizar formulários, personalizar seu dominio nas opções de gerenciamento de dominios e etc..., enfim conseguimos fazer bastante coisa utilizando o deploy com o netlify.
