# ReactJS

## Criar páginas web no Github é algo bem comum fora Brasil mas tem crescido aqui também, seja para você ter a sua página pessoal com seus projetos e trabalhos desenvolvidos, ou informações sobre um projeto open source que você criou.
##### Tiago Fonseca

## Criando sua página

Usaremos o GitHub Pages por ser uma forma de hospedar uma página e ter um domínio de forma gratuita, enquanto o ReactJS acredito ser divertido para criar páginas que não sejam apenas estáticas, além de ser uma tecnologia em alta.

### Pré-requisitos:

- Ter uma conta no GitHub: https://github.com/join
- Git instalado: https://git-scm.com/book/pt-br/v2/Come%C3%A7ando-Instalando-o-Git
- Ter o NodeJS e o NPM instalados: https://nodejs.org/en/

Vamos instalar o pacote create react app, que facilita nossa vida criando os arquivos necessários para iniciar um projeto em ReactJS.

'''
$ npm install -g create-react-app
'''

## 2. Crie um repositório no GitHub e dê um clone:

### Clone o seu repositório para o seu ambiente local
'''
$ git clone <URL_GIT_REPO>
'''
### Entre na pasta gerada com o nome do repositório
'''
$ cd <PASTA_REPO>
'''

## 3. Inicialize o seu projeto com o nome desejado.

'''
$ create-react-app <NOME_DO_PROJETO>
'''

### 4. Instale o pacote gh-pages que é responsável por gerar e enviar para o seu repositório a página criada:

'''
$ npm install --save gh-pages
'''

### 5. Edite o package.json em “homepage” para identificar o caminho que você deseja que sua página seja hospedada e para gerar o build da página com gh-pages adicione os comandos de predeploy e deploy:

'''
{  
  "name": "website",  
  "version": "0.1.0",  
  "private": true,  
  "homepage": "https://tiagoapolo.github.io/",  
  "dependencies": {
    "ajv": "^6.5.3",
    "gh-pages": "^1.2.0",
    "react": "^16.5.0",
    "react-dom": "^16.5.0",
    "react-scripts": "1.1.5"
  },
  "scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test --env=jsdom",
    "eject": "react-scripts eject",
    "predeploy": "npm run build",
    "deploy": "gh-pages -d build"
  }
}
'''

### 6. Hora de fazer o deploy…

'''
$ npm run deploy
'''

Ele criará um branch no seu repositório com o nome “gh-pages” com os arquivos necessários para o GitHub hospedar a sua página, porém você precisará fazer um merge do branch “gh-pages” para o “master”

OBS.: No arquivo index.html já existe o código do Google Analytics na template que disponibilizei, basta trocar a tag [YOUR-ID] pelo id fornecido pela sua conta do Google Analytics.

[Artigo original](https://medium.com/@tiagoapolo/como-criar-uma-p%C3%A1gina-no-github-pages-com-reactjs-fdccba7664cc)