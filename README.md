![blog-header](https://heptetooficial.tumblr.com/private/732088031646023680/tumblr_EgI4nykvoacR1fRmm?ref=_tumblr)

# Blog Hepteto

Uma API simples RESTful com CRUD que fornece dados JSON de título e texto de um post.

:globe_with_meridians: Site de demonstração: https://consumo-api-blog.vercel.app/
:globe_with_meridians: Documentação: https://app.swaggerhub.com/apis-docs/HEPTETOOFICIAL/BLOG_HEPTETO/1.0#/

## Host de produção

[https://api-blog-hepteto.vercel.app](https://api-blog-hepteto.vercel.app)

## API

### `POST /posts`

Cria uma nova postagem no blog com base nos dados fornecidos no corpo da solicitação:

> [https://api-blog-hepteto.vercel.app/posts](https://api-blog-hepteto.vercel.app/posts)


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