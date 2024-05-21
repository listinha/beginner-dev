# 002 - Notação

_Nota: você não precisa conhecer HTML para conseguir resolver este exercício pois você usará somente algumas primitivas básicas da linguagem aqui._

Seus amigos jornalistas do jornal "_O Jornaleco_" já estão cansados de escreve matérias em HTML e tendo que ficar escrevendo coisas como `<strong>` e `<i>` o tempo todo.
Eles sabem que você está em curso de se tornar um mestre da programação e pediram se não poderia escrever uma linguagem mais fácil para eles e um programa que converta desta linguagem para HTML. Disseram que não irão lhe pagar nada pois não há verba na empresa nem para comprar um software decente e por isso eles precisam publicar artigos em formato HTML.

Parte de seu problema já está resolvido, pois foi a linguagem "NT" foi inventada e agora seu trabalho é apenas escrever um programa que converta desta linguagem para a linguagem HTML.

### O Problema

Seu programa deve ler um arquivo em formato "NT" e traduzi-lo para um formato HTML simples.

No formato NT é possível representar textos com marcação **negrito** e _itálico_. Também é possível separar parágrafos e criar listas. Aqui vai uma lista:

- Isto é uma lista!
- Este é o segundo elemento desta lista.
- E este é o último elemento dela. _Há um pouco de itálico aqui_.

Por exemplo, para produzir este parágrafo, a lista acima e o parágrafo acima dela, usa-se o seguinte texto em formato NT:

```markdown
No formato NT é possível
representar
textos com marcação *negrito* e _itálico_.
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

O exemplo acima demonstra todas as características existentes no formato NT. As regras são as seguintes:

- Um texto entre dois underscores ("\_") produz um texto em _itálico_. Em HTML, um texto em itálico inicia em `<i>` e é finalizado em `</i>`.
- Um texto entre dois asteriscos ("*") produz um texto em **negrito**. Em HTML, um texto em negrito inicia em `<strong>` e é finalizado em `</strong>`.
- Quebras de linha simples não interferem na tradução de NT para HTML. Porém duas ou mais quebras de linha sequenciais causam um novo parágrafo. Note no exemplo acima que há 3 parágrafos. Em HTML, um parágrafo é iniciado em `<p>` e finalizado em `</p>`.
- Listas são sempre iniciadas em hífens ("-") e uma lista sempre gera um parágrafo para ela. Veja no exemplo acima para entender! Note que é possível haver listas de um só item. Em HTML, uma lista é iniciada com `<ul>` e finalizada em `</ul>` e cada item da lista é iniciado em `<li>` e finalizado em `</li>`.

O seu programa sempre lerá um arquivo chamado `artigo.nt` e escreverá o resultado na tela.

### Notas

- Em HTML, os items de uma lista sempre devem ficar entre um `<ul>` e um `</ul>`.
- As quebras de linha sequenciais que produzem parágrafos sempre produzem um só parágrafo. Ou seja, duas quebras sequenciais produzem um parágrafo e trinta quebras também produzém apenas um único parágrafo e não trinta deles.
- Dica: você pode salvar a saída HTML do seu programa em um arquivo com extensão `.html` e abrir este arquivo em um navegador web para visualizar o resultado final!
