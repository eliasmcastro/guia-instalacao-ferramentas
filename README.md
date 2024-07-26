<h1 align="center">
  <img alt="Logo" src=".github/undraw_programming.svg" width="250px" />
</h1>

<h3 align="center">
  Ambiente de Desenvolvimento
</h3>

<p align="center">Guia de instalação e configurações das principais ferramentas que eu utilizo no ambiente de desenvolvimento</p>

<p align="center">
  <a href="#sites-essenciais">Sites essenciais</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#ferramentas">Ferramentas</a>
</p>

## Sites essenciais

- [Notion](https://www.notion.so): Ferramenta de anotações
- [Whimsical](https://whimsical.com): Ferramenta para desenhar fluxograma
- [Figma](https://www.figma.com): Ferramenta para Design de Interfaces
- [unDraw](https://undraw.co): É uma plataforma que oferece uma coleção de ilustrações gratuitas desenhadas em SVG

## Ferramentas

A seguir, você encontrará um guia detalhado para a instalação e configuração das principais ferramentas que utilizo em meu ambiente de desenvolvimento. Todos os comandos devem ser executados no PowerShell em modo administrador.

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

O [Composer](https://getcomposer.org/) é um gerenciador de dependências para PHP.

- Como instalar o Composer: `choco install composer`
- Verificar a versão instalada: `composer --version`
- Atualizar a versão do Composer: `choco upgrade composer`