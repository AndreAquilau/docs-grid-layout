## Documentação Grid-Layout

Define o elemento como um contêiner de grade e estabelece um novo contexto de formatação de grade para seu conteúdo.

#### Display-Grid

```css
#main {
  display: grid;
}
```

#### Grid-Template-Areas

- Com Grid-Template-Area já conseguimos montar os grid do nosso layout.
- Passando para cada String o nome do grid.

```css
#container-grid {
  display: grid;
  grid-template-areas:
    "header empty"
    "nav-bar nav-bar"
    "content content"
    "footer footer";
}

.header-grid {
  grid-area: header;
}
.navbar-grid {
  grid-area: navbar;
}
.content-grid {
  grid-area: content;
}
.footer-grid {
  grid-area: footer;
}
```

- No exemplo acima criamos um layout com duas colunas e quatro linhas.


#### Grid-Template-Rows

- Com Grid-Template-Rows podemos definir a largura de cada linha ou row que o layout irá ter.
- Aceita os valores em porcentagem, px, vw, auto e fr;
  > grid-template-rows: **100%** | **100px** | **100vw** | **1fr** | **auto**

```css
#container-grid {
  display: grid;
  grid-template-areas:
    "header empty"
    "nav-bar nav-bar"
    "content content"
    "footer footer";
  grid-template-rows: 20px 20px 60px 20px;
}
```


#### Grid-Template-Columns

- Com Grid-Template-Columns podemos definir a largura de cada coluna ou column que o layout irá ter.
- Aceita os valores em porcentagem, px = pixes, vw = viewportWidth, auto e fr = fração;
- O mais utilizado é fração, **1fr** = uma fração 0 >= 1.
- também podemos utilizar o **reapet(quantidade = 3, valor = 1fr)**
> grid-template-columns: **100%** | **100px** | **100vw** | **1fr** | **auto**


```css
#container-grid {
  display: grid;
  grid-template-areas:
    "header empty"
    "nav-bar nav-bar"
    "content content"
    "footer footer";
  grid-template-columns: 20px 20px 60px 20px;
}
```

#### Grid-Row-Start & Grid-Row-End | Grid-Row
* Grid-Row-Start é uma propriedade definida no item e defini em qual linha do grid ele irá iniciar.
* Grid-Row-End é uma propriedade definida no item e defini em qual linha do grid ele irá termina.
```css
.item-grid {
  /* old */
  grid-row-start: 1;
  grid-row-end: 3
}
```
----------------------------------------------------------------------------------------------------
* Grid-Row é uma propriedade definida no item e defini em qual linha do grid ele irá inciar e finalizar.
* A linha final definida ela não será ocupada __1__/__3__ a tercera linha não será ocupada.
> grid-row: __Start__ /__End__ | __1__/__3__
```css
.item-grid {
  /* standard */
  grid-row: 1/3;
}
```

#### Grid-Column-Start & Grid-Column-End | Grid-Column
* Grid-Column-Start é uma propriedade definida no item e defini em qual coluna do grid ele irá iniciar.
* Grid-Column-End é uma propriedade definida no item e defini em qual coluna do grid ele irá termina.
```css
.item-grid {
  /* old */
  grid-column-start: 1;
  grid-column-end: 3
}
```
----------------------------------------------------------------------------------------------------
* Grid-Column é uma propriedade definida no item e defini em qual coluna do grid ele irá inciar e finalizar.
* A coluna final definida ela não será ocupada __1__/__3__ a tercera Coluna não será ocupada.
> grid-column: __Start__ /__End__ | __1__/__3__
```css
.item-grid {
  /* standard */
  grid-column: 1/3;
}
```

#### Grid-Column-Gap & Column-Gap
* Grid-Column-Gap é uma propriedade de espaçamento de uma coluna da outra.
* É definida no container.
* Aceita valores em __px__, __%__.
```css

.container-grid {
  /* old */
  grid-column-gap: 5px;

  /* standard */
  column-gap: 5px;
}
```
#### Grid-Row-Gap & Row-Gap
* Grid-Row-Gap é uma propriedade de espaçamento de uma linha da outra.
* É definida no container.
* Aceita valores em __px__, __%__.

```css
.container-grid {
  /* old */
  grid-row-gap: 5px;

  /* standard */
  row-gap: 5px;

}
```


#### Align-Self - Vertical
* É o alinhamento do conteudo dos items dentro das celulas.
* É um alinhamento Vertical ou seja no eixo Y.
* É definido no item, default __stretch__.
> start | end | center | stretch;
```css
.item-grid {
  align-self: start | end | center | stretch;
}
```

#### Justify-Self - Horizontal
* É o alinhamento do conteudo dos items dentro das celulas.
* É um alinhamento horizontal ou seja no eixo principal X.
* É definido no item, default __stretch__.
> start | end | center | stretch;
```css
.item-grid {
  justify-self: start | end | center | stretch;
}
```

#### Place-Self - Horizontal & Vertical
* É o alinhamento do conteudo dos items dentro das celulas.
* É um alinhamento na horizontal e na vertical em uma única propriedade.
* É definido no item, default __stretch__.
> start | end | center | stretch;
```css
.item-grid {
  place-self: start | end | center | stretch;
}
```

#### References
- [complete-guide-grid](https://css-tricks.com/snippets/css/complete-guide-grid/)
- [layoutit - gerador de layout-code-font](https://grid.layoutit.com/)
