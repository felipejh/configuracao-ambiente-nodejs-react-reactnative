# Ambiente de desenvolvimento NodeJS, React, React Native

## Fonte

### Baixar a fonte JetBrains Mono

[Download](https://download.jetbrains.com/fonts/JetBrainsMono-1.0.0.zip?_ga=2.251810441.1239792011.1579725382-1768142081.1576204351)

## VS Code

### Instalar extensões

- Tema Drácula
- Material Icon Theme

### Substituir todo o conteúdo do arquivo de configuração pelo conteúdo abaixo.

O arquivo pode ser acesso a partir de:
> Code -> Prefences -> Settings

``` 
{
    // Altera o tema e ícones
    "workbench.colorTheme": "Dracula",
    "workbench.iconTheme": "material-icon-theme",

    "editor.fontSize" : 14,
    "editor.fontFamily": "JetBrains Mono",
    "editor.fontLigatures": true,

    // Terminal no VSCode
    "terminal.integrated.shell.osx": "/bin/zsh",
    "terminal.integrated.fontSize" : 14,

    // Codificação de texto
    "files.encoding": "utf8bom",
    "files.autoGuessEncoding": true,

    // Usar div.input-group
    "emmet.syntaxProfiles": {
        "javascript": "jsx",
    },
    "emmet.includeLanguages": {
        "javascript": "javascriptreact",
    },

    // Máximo de caracteres por linha
    "editor.rulers" : [80, 120],

    // Destaca a linha apenas na direita
    "editor.renderLineHighlight" : "gutter",

    // Tamanho da coluna na esquerda
    "editor.tabSize": 2,

    "editor.parameterHints.enabled": false,
    "javascript.updateImportsOnFileMove.enabled": "never",
    "javascript.suggest.autoImports": false,

    // Caminho do arquivo no título
    "breadcrumbs.enabled" : true,
} 
```

## Terminal

### Alterar a fonte do terminal para JetBrains Mono, nas configurações.

### Tema

Instalar o tema Dracula a partir do link abaixo:

[Dracula Theme](https://draculatheme.com/terminal/)

### Oh My Zsh

#### Instalação

``` $ sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)" ```

#### Tema Spaceship para o Oh My Zsh

##### Instalação 
``` git clone https://github.com/denysdovhan/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt" ```

``` ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme" ```

##### Setar o tema

1. Abrir o arquivo de configuração:

``` sudo nano ~/.zshrc ```

2. Alterar a linha:

``` ZSH_THEME="spaceship" ```

##### Configurações adicionais do Spaceship

1. Abrir o arquivo de configuração

``` sudo nano ~/.zshrc ```

2. Incluir as linhas abaixo:
```
SPACESHIP_PROMPT_ORDER=(
  user          # Username section
  dir           # Current directory section
  host          # Hostname section
  git           # Git section (git_branch + git_status)
  hg            # Mercurial section (hg_branch  + hg_status)
  exec_time     # Execution time
  line_sep      # Line break
  vi_mode       # Vi-mode indicator
  jobs          # Background jobs indicator
  exit_code     # Exit code section
  char          # Prompt character
)
SPACESHIP_USER_SHOW=always
SPACESHIP_PROMPT_ADD_NEWLINE=false
SPACESHIP_CHAR_SYMBOL="❯"
SPACESHIP_CHAR_SUFFIX=" "
```

### Plugins

#### Z-Plugin

```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/zdharma/zinit/master/doc/install.sh)"
```

Após essa instalação, vamos abrir o arquivo ``` ~/.zshrc ``` novamente e abaixo da linha ``` ### End of Zplugin's installer chunk``` que foi adicionada automaticamente no arquivo, adicionamos:

```
zplugin light zdharma/fast-syntax-highlighting
zplugin light zsh-users/zsh-autosuggestions
zplugin light zsh-users/zsh-completions
```

## Ferramentas

### Insomnia

Ferramenta para testes de requisições à API
[Download](https://insomnia.rest/)

### DevDocs

Ferramenta com documentação de várias linguagens
[Download](https://devdocs.egoist.moe/)

