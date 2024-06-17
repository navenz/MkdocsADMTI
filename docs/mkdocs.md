# Introdução ao MkDocs

MkDocs é uma ferramenta para a criação de sites estáticos, ideal para a documentação de projetos. Desenvolvido em Python, o MkDocs é conhecido por ser simples e eficiente, permitindo que desenvolvedores e equipes técnicas criem e mantenham documentações de alta qualidade com pouco esforço. Usamos o MkDocs para documentar os sistemas que utilizamos durante o período.

## Instalação do MkDocs

### Primeiro Passo

Para instalar o MkDocs no Windows, é necessário ter o Python e o pip instalados. Para saber mais, [CLIQUE AQUI](https://www.python.org/downloads/). Com o Python e o pip instalados, verifique se estão funcionando usando os comandos `python --version` e `pip --version`. Se as versões aparecerem, está tudo certo.

### Segundo Passo

Abra o **PowerShell** como administrador e execute o comando `pip install mkdocs`. Isso instalará o MkDocs e permitirá que você crie novos projetos.

### Terceiro Passo

Para criar um novo projeto e entrar nele, execute o comando `mkdocs new my-project` e depois `cd my-project` para entrar na pasta do projeto.

### Quarto Passo

Veja seu site no navegador usando o comando `mkdocs serve`. Copie a URL gerada e cole no navegador para visualizar. Pronto, agora você está usando o MkDocs.

### Quinto Passo

Antes de configurar o **mkdocs.yml**, você pode instalar um tema personalizado. No meu caso, usei o tema MkDocs Material. Para instalá-lo, execute `pip install mkdocs-material`. Agora, você pode utilizar as funcionalidades que o tema oferece.

## Configuração

Aqui, explicarei como configurei e personalizei minha documentação. A seguir, o passo a passo.
### Primeiro Passo

`site_name: Documentação dos Sitemas` -> Aqui você pode dar o nome que você quiser para o seu site.

### Segundo Passo

```
nav:
  - Home: index.md
  - Sobre: about.md
  - Introdução: intro.md
  - GLPI: glpi.md
  - MkDocs: mkdocs.md
  - Conclusão: conclusao.md
```
Essa é a estrutura de navegação para as páginas do seu documento.

### Terceiro Passo

```
theme:
  name: material // tema escolhido
  palette:  // Palleta de cores
    # Light mode
    - scheme: default
      primary: teal
      accent: pink
      toggle:
        icon: material/toggle-switch 
        name: Switch to dark mode

    # Dark mode
    - scheme: slate
      primary: pink
      accent: teal
      toggle:
        icon: material/toggle-switch-off-outline
        name: Switch to light mode
  font:
     text: Roboto Mono  
  language: pt-BR 
  features:
    - search.suggest // Sugestões de resultados na pesquisa.

    - search.share // Permissão para compartilhamento.
    - navigation.instant  //  Troca instantânea na navegação, garantindo fluidez.
    - navigation.instant.prefetch  // Prevê trocas de páginas, garantindo velocidade.
  
  extra_css:
    - stylesheets/extra.css 
   social:
    - icon: fontawesome/brands/mastodon 
      link: https://fosstodon.org/@squidfunk
    - icon: fontawesome/brands/mastodon
      link: https://fosstodon.org/@squidfunk
```
### Quarto Passo 

```
plugins:  // pliugins para o search
  - search

```

Com isso você terá todas as suas funcionalidades que eu tive para fazer está documentação.