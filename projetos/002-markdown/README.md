# 002 - Notação


### O Problema

Seu programa deve ler um arquivo em formato "NT" e traduzi-lo para um formato HTML simples. Nota: você não precisa conhecer HTML para conseguir resolver este exercício pois você usará somente algumas primivitas básicas da linguagem aqui.

No formato NT é possível representar textos com marcação **negrito** e _itálico_. Também é possível separar parágrafos e criar listas. Aqui vai uma lista:

- Isto é uma lista!
- Este é o segundo elemento desta lista.
- E este é o último elemento dela. _Há um pouco de itálico aqui_.

Por exemplo, para produzir este parágrafo, a lista acima e o parágrafo acima dela, usa-se o seguinte texto em formato NT:

```markdown
No formato NT é possível
representar
textos com marcação **negrito** e _itálico_.
Também é possível separar parágrafos e criar listas. Aqui vai uma lista:

- Isto é uma lista!
- Este é o segundo elemento desta lista.
- E este é o último elemento dela. _Há um pouco de itálico aqui_.

Por exemplo, para produzir este parágrafo,
a lista acima e o parágrafo acima dela, usa-se o seguinte texto em formato NT:
```

A tradução para HTML do NT acima é o seguinte:

```html
<p>No formato NT é possível representar textos com marcação <strong>negrito</strong> e <i>itálico</i>. Também é possível separar parágrafos e criar listas. Aqui vai uma lista:</p>

<p>
<ul>
<li>Isto é uma lista!</li>
<li>Este é o segundo elemento desta lista.</li>
<li>E este é o último elemento dela. <i>Há um pouco de itálico aqui</i>.</li>
<li>
</ul>
</p>

<p>Por exemplo, para produzir este parágrafo, a lista acima e o parágrafo acima dela, usa-se o seguinte texto em formato NT:</p>
```