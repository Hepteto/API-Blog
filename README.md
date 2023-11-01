![header](https://64.media.tumblr.com/1f0cd74f2e5445179f210df582f5f2d4/73e6902468f719e5-fd/s640x960/838d92d1bc97707f8f888b62d9de98d82354c71c.pnj)

# API Blog

Uma API simples RESTful com CRUD que fornece dados JSON de título e texto de um post.
<br /><br />
:globe_with_meridians: Site de demonstração: https://consumo-api-blog.vercel.app/
<br />
:globe_with_meridians: Documentação: https://app.swaggerhub.com/apis-docs/HEPTETOOFICIAL/BLOG_HEPTETO/1.0#/

## Host de produção

[https://api-blog-hepteto.vercel.app](https://api-blog-hepteto.vercel.app)

## API

### `POST /posts`

Cria uma nova postagem no blog com base nos dados fornecidos no corpo da solicitação:

> [https://api-blog-hepteto.vercel.app/posts](https://api-blog-hepteto.vercel.app/posts)
<br />
Exemplo de valor:

    {
        "title": "Título do Post",
        "body": "Texto corpo do post."
    }


### `GET /posts`

Retorna uma lista de todas as postagens no blog:

> [https://api-blog-hepteto.vercel.app/posts](https://api-blog-hepteto.vercel.app/posts)

    [
        {
            "_id":"6529541abdf3126d15dfd405",
            "title":"Problemas",
            "body":"Os problemas são oportunidades para se mostrar o que sabe",
            "__v":0
        },   
        {
            "_id":"6529542dbdf3126d15dfd407",
            "title":"Express",
            "body":" ",
            "__v":0
        }
    ]
    

### `GET /posts/{id}`

Retorna os detalhes de uma postagem específica com base no `id`:

> [https://api-blog-hepteto.vercel.app/posts/6529541abdf3126d15dfd405](https://api-blog-hepteto.vercel.app/posts/6529541abdf3126d15dfd405)

    [
        {
            "_id":"6529541abdf3126d15dfd405",
            "title":"Problemas",
            "body":"Os problemas são oportunidades para se mostrar o que sabe",
            "__v":0
        }
    ]

### `PATCH /posts/{id}`

Atualiza uma postagem existente com base no `id` com os dados fornecidos no corpo da solicitação:

> [https://api-blog-hepteto.vercel.app/posts/6529541abdf3126d15dfd405](https://api-blog-hepteto.vercel.app/posts/6529541abdf3126d15dfd405)
<br />
Exemplo de valor:

    {
        "title": "Título do Post a ser atualizado",
        "body": "Texto corpo do post a ser atualizado."
    }


### `DELETE /posts/{id}`

Exclui uma postagem existente com base no `id`:

> [https://api-blog-hepteto.vercel.app/posts/6529541abdf3126d15dfd405](https://api-blog-hepteto.vercel.app/posts/6529541abdf3126d15dfd405)

    {
        "message: "Post removido com sucesso",
    }
