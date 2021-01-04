# Todo

My first Elixir app is a Todo list API using Phoenix & GraphQL.

To start your Phoenix server:

  * Install dependencies with `mix deps.get`
  * Create and migrate your database with `mix ecto.setup`
  * Install Node.js dependencies with `npm install` inside the `assets` directory
  * Start Phoenix endpoint with `mix phx.server`

Now you can visit [`localhost:4000`](http://localhost:4000) from your browser.

Ready to run in production? Please [check our deployment guides](https://hexdocs.pm/phoenix/deployment.html).

## Routes

The API playground can be located at: http://localhost:4000/api

### Get TodoItems

```
{
  todoItems {
    id content
  }
}
```

### Create TodoItem

```
mutation createTodoItem($content: String!) {
  createTodoItem(content: $content)
}
```

**Query Variable**

```
{
  "content": "Talk to Rune about a Video Cast"
}
```

### Toggle Todo Item

*Mark as completed*

```
mutation($id: ID!) {
  toggleTodoItem(id: $id) {
    id content isCompleted
  }
}
```

**Query Variable**

```
{
  "id": 2
}
```

## Todo
- [x] Create Elixir app.
- [x] Create the GraphQL API
- [ ] Deploy to Heroku
- [ ] Create a frontend using NuxtJS or NextJS to learn any of these 2 frameworks.
- [ ] Create a video cast to show the steps taken to create this app.

## Learn more

  * Official website: https://www.phoenixframework.org/
  * Guides: https://hexdocs.pm/phoenix/overview.html
  * Docs: https://hexdocs.pm/phoenix
  * Forum: https://elixirforum.com/c/phoenix-forum
  * Source: https://github.com/phoenixframework/phoenix
