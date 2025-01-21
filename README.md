<h1 align="center">
  <img alt="Logo" src=".github/undraw_programming.svg" width="250px" />
</h1>

<h3 align="center">
  Ambiente de Desenvolvimento
</h3>

<p align="center">Guia de instalação e configurações das principais ferramentas que eu utilizo no ambiente de desenvolvimento</p>

<p align="center">
  <a href="#sites-essenciais">Sites essenciais</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#ferramentas">Ferramentas</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#problemas">Problemas</a>
</p>

## Sites essenciais

- [Notion](https://www.notion.so): Ferramenta de anotações
- [Whimsical](https://whimsical.com): Ferramenta para desenhar fluxograma
- [Figma](https://www.figma.com): Ferramenta para Design de Interfaces
- [unDraw](https://undraw.co): É uma plataforma que oferece uma coleção de ilustrações gratuitas desenhadas em SVG

## Ferramentas

A seguir, você encontrará um guia detalhado para a instalação e configuração das principais ferramentas que utilizo em meu ambiente de desenvolvimento. Todos os comandos devem ser executados no PowerShell em modo administrador.

- <a href="#chocolatey">Chocolatey</a>
- <a href="#nodejs--nmv">Node.js + nmv</a>
- <a href="#yarn">Yarn</a>
- <a href="#composer">Composer</a>
- <a href="#insomnia">Insomnia</a>
- <a href="#docker-e-docker-compose">Docker e Docker Compose</a>
- <a href="#eslint-e-prettier-para-nodejs">ESLint e Prettier para Node.js</a>
- <a href="#visual-studio-code">Visual Studio Code</a>

### Chocolatey

- O [Chocolatey](https://chocolatey.org) é gerenciador de pacotes para Windows e com ele é possível você instalar e remover facilmente programas (ex: nvm, node, java).

- Como instalar o Chocolatey: Seguir o [guia de instalação](https://chocolatey.org/install) do prório Chocolatey.

- Principais comandos:
  - `choco list --local-only`: Listar os pacotes instalados localmente
  - `choco install <pacote_nome>`: Para instalar um pacote
  - `choco uninstall <pacote_nome>`: Para remover um pacote

### Node.js + nmv

- O `nvm` (Node Version Manager) é uma ferramenta que permite gerenciar várias versões do `Node.js` no mesmo sistema. Para Windows, podemos utilizar o [nvm-windows](https://github.com/coreybutler/nvm-windows).

- Como instalar o nmv-windows: `choco install nvm`

- Como instalar e gerenciar versões do Node.js com nvm
  - `nvm install <version>` para instalar uma versão do Node.js
    - Ex: `nvm install v20.16.0`
  - `nvm list` para visualizar todas as versões instaladas do Node.js
  - `nvm use <version>` para usar uma versão do Node.js
  - `nvm uninstall <version>` para remover uma versão do Node.js
  - `node -v` para visualizar a versão que está sendo utilizada do Node.js
  - `npm -v` para visualizar a versão que está sendo utilizada do npm

### Yarn

O [Yarn](https://yarnpkg.com) é um gerenciador de dependências para projetos JavaScript e Node.js e é semelhante ao `npm`, mas é conhecido por ser mais rápido. Atualmente utilizo a [versão clássica](https://classic.yarnpkg.com/en).

- Como instalar o Yarn: `choco install yarn`
- Verificar a versão instalada: `yarn -v`
- Atualizar a versão do Yarn: `choco upgrade yarn`

### Composer

O [Composer](https://getcomposer.org) é um gerenciador de dependências para PHP.

- Como instalar o Composer: `choco install composer`
- Verificar a versão instalada: `composer --version`
- Atualizar a versão do Composer: `choco upgrade composer`

### Insomnia

O [Insomnia](https://insomnia.rest) é uma ferramenta para testar APIs, acesse o site e baixe a versão adequada para o seu sistema operacional

### Docker e Docker Compose

O [Docker](https://www.docker.com) é uma plataforma para criar e gerenciar contêineres que encapsulam aplicações e suas dependências, enquanto [Docker Compose](https://docs.docker.com/compose) é uma ferramenta para definir e executar multi-contêineres Docker usando um único arquivo de configuração.

Acesse o [guia](https://efficient-sloth-d85.notion.site/Docker-e-Docker-Compose-16771f2ceefe4a05a8c29df4ca49e97a) de como instalar o Docker e Docker Compose nos principais sistemas operacionais

### ESLint e Prettier para Node.js

Acesse o [guia](https://efficient-sloth-d85.notion.site/ESLint-e-Prettier-Trilha-Node-js-d3f3ef576e7f45dfbbde5c25fa662779) e veja o passo a passo de como realizar a configuração do ESLint, Prettier e EditorConfig para Node.js

Nota: Foi necessário adicionar essa regra "editor.formatOnSave": false no settings.json do VSCode para funcionar

### Visual Studio Code

O [Visual Studio Code (VS Code)](https://code.visualstudio.com) é um editor de código-fonte desenvolvido pela Microsoft, acesse o site e baixe a versão adequada para o seu sistema operacional

- Fontes
  - [Fira Code](https://github.com/tonsky/FiraCode)
- Extensões
  - Dracula Theme Official (Dracula Theme)
  - Material Icon Theme (Philipp Kief)
  - Color Highlight (Sergii N)
  - Live Server (Ritwick Dey)
  - EditorConfig for VS Code (EditorConfig)
  - Prettier - Code formatter (Prettier)
  - ESLint (Microsoft)
  - Vetur (Pine Wu)
  - PHP DocBlocker (Neil Brayfield)
  - PHP Intelephense (Ben Mewburn)
  - SQLite (alexcvzz)
  - vscode-styled-components (Styled Components)
- Configurações
  - Ctrl + Shift + P → Abrir o arquivo Open User Settings (JSON)
  - Consulte o arquivo settings.json para ver minhas configurações

## Problemas

A seguir, você encontrará instruções para corrigir alguns problemas comuns no ambiente de desenvolvimento.

- <a href="#wampserver-curl-error-60-ssl-certificate-unable-to-get-local-issuer-certificate">WampServer cURL error 60: SSL certificate: unable to get local issuer certificate</a>

### WampServer cURL error 60: SSL certificate: unable to get local issuer certificate

Se, ao usar cURL no PHP com o [WampServer](https://wampserver.aviatechno.net), você encontrar o erro `cURL error 60: SSL certificate: unable to get local issuer certificate`, siga os passos abaixo para resolver o problema:

- Baixe o [pacote de certificados](https://curl.se/docs/caextract.html)
  - Arquivo `cacert.pem`
- Coloque o pacote na pasta: `C:\wamp64\bin\php\your-php-version\extras\ssl`
- Certifique-se de que o arquivo `mod_ssl.so` esteja na pasta: `C:\wamp64\bin\apache\your-apache-version\modules`
- Habilite o `mod_ssl` no arquivo `httpd.conf` localizado em: `C:\wamp64\bin\apache\your-apache-version\conf`
- Habilite a extensão `openssl` no arquivo `php.ini`. É necessário fazer essa alteração em dois locais diferentes:
  - O primeiro local pode ser acessado através do ícone `WampServer -> PHP -> php.ini` na barra de tarefas do Windows
  - O segundo local está em `C:\wamp64\bin\php\your-php-version`
- Ainda no arquivo `php.ini` dos dois locais
  - Encontre as linhas `curl.cainfo` e `openssl.cafile` e atualize ambas para:
    - `curl.cainfo="C:\wamp64\bin\php\your-apache-version\extras\ssl\cacert.pem"`
    - `openssl.cafile="C:\wamp64\bin\php\your-apache-version\extras\ssl\cacert.pem"`
- Após fazer essas alterações, salve os arquivos e reinicie o servidor.