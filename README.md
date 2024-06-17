# static-webdev-toolkit

Static-WebDev-Toolkit: Um kit completo para desenvolvimento de sites estáticos modernos usando Vite, TailwindCSS e Alpine.js.  Ele inclui um sistema de versionamento dinâmico e um servidor para testar builds de produção localmente.

### Estrutura do Projeto

- `src/`: Contém os arquivos fonte do projeto (HTML, CSS, JS).
- `releases/`: Diretório onde as builds de produção são armazenadas, organizadas por versão.
- `scripts/`: Scripts personalizados para gerenciamento de versão e servidor de produção.
- `public/`: Arquivos estáticos públicos.

### Tecnologias utilizadas:
- Tailwind
- Alpine.js
- Vite

### Instalação

Primeiro, clone o repositório e instale as dependências:

```bash
git clone https://github.com/seu-usuario/seu-repositorio.git
cd seu-repositorio
npm install
```

### Configuração do TailwindCSS

O projeto já está configurado para usar TailwindCSS. O arquivo tailwind.config.js está configurado para monitorar arquivos em ./src/**/*.{html,js}. O arquivo postcss.config.js inclui tailwindcss e autoprefixer.


### Sistema de Branch

O projeto utiliza o sistema de branch para gerenciar o desenvolvimento de novas funcionalidades, correções de bugs e outras alterações no código. O fluxo de trabalho com branches é o seguinte:

1. Cada nova funcionalidade ou correção de bug é desenvolvida em uma branch separada.
2. As branches são criadas a partir da branch principal (geralmente chamada de "main" ou "master").
3. Após concluir o desenvolvimento e testes na branch, é feito um merge da branch com a branch principal.
4. Caso necessário, é feita uma revisão do código antes de realizar o merge.
5. Após o merge, a branch pode ser excluída.

Esse sistema de branch permite um desenvolvimento mais organizado e seguro, evitando conflitos entre diferentes funcionalidades e facilitando a colaboração entre os membros da equipe.

#### Exemplo de git

Aqui estão alguns exemplos de comandos git para criar e mesclar branches de funcionalidade e correção de bugs:

##### Criar branch de funcionalidade

```bash
git checkout develop
git checkout -b feature/nome-da-funcionalidade
git push -u origin feature/nome-da-funcionalidade
```
##### Mesclar uma Brach de funcionalidade

```bash
git checkout develop
git pull origin develop
git merge feature/nome-da-funcionalidade
git push
```

##### Criar uma Branch de Corriçao de Bug

```bash
git checkout develop
git checkout -b bugfix/nome-do-bug
git push -u origin bugfix/nome-do-bug
```

##### Mesclar uma Branch de Correção de Bug

```bash
git checkout develop
git pull origin develop
git merge bugfix/nome-do-bug
git push
```


## Scripts NPM

### Desenvolvimento

Para iniciar o servidor de desenvolvimento com hot reload.

```bash
npm run dev
```

### Build de Produção

Para criar uma build de produção:
Incremental minor:

```bash
npm run prebuild:minor && npm run build
```

####  major:
```bash
npm run prebuild:major && npm run build
```

### Servir uma Versão Específica

```bash
npm run serve:prod -- v0.2.1
```
# static-webdev-toolkit
Static-WebDev-Toolkit: Um kit completo para desenvolvimento de sites estáticos modernos usando Vite, TailwindCSS e Alpine.js. Inclui automações e configurações otimizadas.
