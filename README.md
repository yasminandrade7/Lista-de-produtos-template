# Lista de Produtos — Consumindo JSON com JavaScript

**Professor:** Fernando Leonid

---

## Objetivo da Atividade

Esta atividade tem como objetivo consolidar o aprendizado de **transformar dados JSON em HTML** (consumir JSON). Este é um conceito fundamental que serve como base para, futuramente, aprender a **consumir APIs REST**.

---

## Descrição

O aluno deverá criar uma **lista de cards de produtos** a partir dos dados do arquivo `produtos.json`, utilizando HTML, CSS e JavaScript puro.

### Requisitos

1. **Leitura do JSON**
   - Carregar os dados do arquivo `produtos.json` utilizando `import` com atributo de tipo:
     ```js
     import produtos from "./produtos.json" with { type: "json" }
     ```
   - Iterar sobre os produtos e gerar os cards dinamicamente no HTML.

2. **Cards de Produtos**
   Cada card deve exibir:
   - Imagem do produto (pasta `img/`)
   - Nome do produto
   - Descrição
   - Preço (formatado em R$)
   - Categoria
   - Classificação em estrelas

3. **Destaque por Categoria**
   - Cada **categoria** deve ser visualmente diferenciada. Exemplos:
     - Uma faixa colorida na parte inferior do card
     - O card inteiro com uma cor de fundo
   - As categorias presentes no JSON são: **Informática** e **Eletrônicos**

4. **Classificação com Estrelas**
   - O campo `classificacao` é um número de 1 a 5.
   - Deve ser representado visualmente com **estrelas** (★ preenchidas e ☆ vazias).
   - Exemplo: classificação `3` → ★★★☆☆

5. **Animação no Hover**
   - Ao passar o mouse sobre o card, deve haver algum tipo de **animação CSS**.
   - Exemplos: escala (`transform: scale`), sombra (`box-shadow`), elevação, mudança de cor, etc.

---

## Estrutura do Projeto

```
├── index.html        # Página principal
├── style.css         # Estilos dos cards e layout
├── produtos.json     # Dados dos produtos
├── README.md         # Este arquivo
└── img/              # Imagens dos produtos
    ├── notebook-dell-inspiron-15-3000.png
    ├── monitor-samsung-led-23.8.png
    ├── mouse-gamer-logitech-g-pro.png
    ├── teclado-mecanico-redragon-kumara.png
    ├── smartphone-samsung-galaxy-s21.png
    ├── tablet-apple-ipad-pro.png
    ├── caixa-de-som-jbl-flip-5.png
    ├── fone-de-ouvido-bluetooth-jbl-tune-500bt.png
    ├── smartwatch-samsung-galaxy-watch-3.png
    └── camera-sony-alpha-a7-iii.png
```

---

## Exemplo de Objeto no JSON

```json
{
  "id": 1,
  "nome": "Notebook Dell Inspiron 15 3000",
  "descricao": "Notebook com processador Intel Core i5, 8GB de RAM e 256GB de SSD",
  "preco": 3999.99,
  "imagem": "notebook-dell-inspiron-15-3000.png",
  "categoria": "Informática",
  "classificacao": 2
}
```

---

## Tecnologias Utilizadas

- HTML5
- CSS3 (Flexbox/Grid, Transitions, Hover)
- JavaScript (import, DOM Manipulation)

---

## Como Executar

1. Faça um fork, clone ou baixe este repositório.
2. Abra o arquivo `index.html` com o **Live Server** (extensão do VS Code) ou qualquer servidor local.
   > **Nota:** O `import` não funciona abrindo o arquivo diretamente no navegador (`file://`). É necessário um servidor HTTP.
