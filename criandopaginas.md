# Criando Páginas

Se você precisar de mais páginas, basta criar mais arquivos markdown em seu diretório docsify. Se você criar um arquivo chamado `guia.md`,  então ele estará acessível via `/#/guia`.

Por exemplo, em uma estrutura de diretórios como a seguinte:

```text
.
└── docs
    ├── README.md
    ├── guia.md
    └── zh-cn
        ├── README.md
        └── guia.md
```


## Barra Lateral
Para ter uma barra lateral, você pode criar sua própria adicionando um arquivo: `_sidebar.md` no seu diretório, como por exemplo:

Primeiro, você precisa definir `loadSidebar` como **true** no seu arquivo ``index.html``. Veja:

```html
<!-- index.html -->

<script>
  window.$docsify = {
    loadSidebar: true
  }
</script>
<script src="//cdn.jsdelivr.net/npm/docsify/lib/docsify.min.js"></script>
```

Depois, crie o arquivo `_sidebar.md` no seu diretório e insira os itens que aparecerão na barra lateral:

```markdown
<!-- docs/_sidebar.md -->

* [Home](/)
* [Guia](guia.md)
```

Você precisa criar um `.nojekyll` no seu diretório docsify para evitar que o GitHub Pages ignore arquivos que começam com um sublinhado.

!> Docsify apenas procura `_sidebar.md` na pasta atual, e usa isso, caso contrário ele volta para o configurado usando a configuração `window.$docsify.loadSidebar`.

Exemplo de estrutura de arquivo:

```text
└── docs/
    ├── _sidebar.md
    ├── index.md
    ├── getting-started.md
    └── running-services.md
```


## Definir títulos de página da barra lateral

Esta função é para adicionar títulos nos itens da barra lateral, isto é, quando o cursor do mouse passar sobre o nome da seção, a leganda com o título aparecer.Você pode personalizar o título especificando uma string após o nome do arquivo. Veja o exemplo:

```markdown
<!-- docs/_sidebar.md -->
* [Home](/)
* [Guia](guide.md "Guia de documentação")
```

## índice

Depois de criar `_sidebar.md`, o conteúdo da barra lateral é gerado automaticamente com base nos cabeçalhos dos arquivos markdown.

Uma barra lateral personalizada também pode gerar automaticamente um índice definindo um `subMaxLevel`. Por padrão, o valor do `subMaxLevel` é 6, portanto você deve indicar o nível que deseja. NO exemplo abaixo, o `subMaxLevel` foi definido como 2.

```html
<!-- index.html -->

<script>
  window.$docsify = {
    loadSidebar: true,
    subMaxLevel: 2
  }
</script>
<script src="//cdn.jsdelivr.net/npm/docsify/lib/docsify.min.js"></script>
```

## Ignorando subtítulos

Quando `subMaxLevel` é definido, cada cabeçalho é adicionado automaticamente ao índice por padrão. Se você quiser ignorar um cabeçalho específico, adicione `<!-- {docsify-ignore} -->` a ele.

```markdown
# Getting Started

## Header <!-- {docsify-ignore} -->

Este cabeçalho não aparecerá no índice da barra lateral.
```

Para ignorar todos os cabeçalhos em uma página específica, você pode usar `<!-- {docsify-ignore-all} -->` no primeiro cabeçalho da página.

```markdown
# Getting Started <!-- {docsify-ignore-all} -->

## Header

Este cabeçalho não aparecerá no índice da barra lateral.
```

Ambos `<!-- {docsify-ignore} -->` e `<!-- {docsify-ignore-all} -->` não será renderizado na página quando usado.

