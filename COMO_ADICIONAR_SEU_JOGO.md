# 🎮 Como adicionar um jogo ao catálogo

O catálogo aceita jogos hospedados neste repositório e jogos publicados em projetos externos.
Nos dois casos, o cadastro é feito no array `GAMES` do `index.html`.

## Opção 1: projeto externo no GitHub Pages

Confirme que a URL final usa HTTPS, abre sem autenticação e termina com `/`. Depois adicione:

```js
{
  url: 'https://inteligenciamilgrau.github.io/meujogo/',
  capa: 'capas/meu_jogo.png',
  titulo: 'Nome do Jogo',
  descricao: 'Uma frase curta apresentando o jogo.',
  categoria: 'Aventura 2D',
  autor: 'Inteligência Mil Grau',
  sigla: 'NJ',
  corAvatar: 'linear-gradient(135deg,#7c3aed,#2563eb)',
  data: 'GitHub Pages',
  tags: ['Aventura','2D','Web'],
  selo: 'Online',
  externo: true
},
```

Entradas externas abrem em uma nova aba. A capa fica neste repositório, mas o clique leva ao
projeto publicado no GitHub Pages. Se ainda não houver uma imagem, `corCapa` + `icone` podem
ser usados temporariamente como arte gráfica.

## Opção 2: jogo hospedado neste repositório

Adicione o HTML em `jogos/`, a capa 1280×720 em `capas/` e cadastre:

```js
{
  url: 'jogos/meu_jogo.html',
  capa: 'capas/meu_jogo.png',
  titulo: 'Nome do Jogo',
  descricao: 'Uma frase curta apresentando o jogo.',
  categoria: 'Corrida 3D',
  autor: 'Nome do modelo de IA',
  sigla: 'NJ',
  corAvatar: 'linear-gradient(135deg,#ef4444,#f59e0b)',
  data: 'agosto de 2026',
  tags: ['Corrida','3D','Web'],
  selo: 'Local'
},
```

Entradas locais abrem na mesma aba e usam a imagem informada em `capa`.

## Campos comuns

| Campo | Descrição |
|---|---|
| `url` | URL externa ou caminho local do jogo |
| `titulo` | Nome exibido no card |
| `descricao` | Resumo curto do projeto |
| `categoria` | Tipo principal do jogo |
| `autor` | Canal, pessoa ou modelo de IA responsável pelo jogo |
| `sigla` | Duas ou três letras para o avatar |
| `corAvatar` | Gradiente CSS do avatar |
| `data` | Data ou origem exibida no card |
| `tags` | Categorias; as três primeiras aparecem no card |
| `selo` | `Online` para externo ou `Local` para hospedado aqui |

Os campos são renderizados como texto. Não insira tags HTML nos valores.

## Checklist

- [ ] O jogo abre pelo endereço cadastrado.
- [ ] A entrada externa tem `externo: true` e uma `capa` (ou o fallback `corCapa` + `icone`).
- [ ] A entrada local tem `capa`, e o arquivo existe em `jogos/`.
- [ ] O título e a descrição estão em português do Brasil.
- [ ] A sigla tem no máximo três caracteres.
- [ ] O card aparece corretamente no hero e na biblioteca.

Depois, abra um pull request no repositório
[inteligenciamilgrau/jogoscomia](https://github.com/inteligenciamilgrau/jogoscomia).
