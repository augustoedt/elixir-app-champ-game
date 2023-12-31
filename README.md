# Champions

To start your Phoenix server:

  * Run `mix setup` to install and setup dependencies
  * Start Phoenix endpoint with `mix phx.server` or inside IEx with `iex -S mix phx.server`

Now you can visit [`localhost:4000`](http://localhost:4000) from your browser.

Ready to run in production? Please [check our deployment guides](https://hexdocs.pm/phoenix/deployment.html).

## Learn more

  * Official website: https://www.phoenixframework.org/
  * Guides: https://hexdocs.pm/phoenix/overview.html
  * Docs: https://hexdocs.pm/phoenix
  * Forum: https://elixirforum.com/c/phoenix-forum
  * Source: https://github.com/phoenixframework/phoenix

## Docker

```bash
docker run -d --name champ -p 5432:5432 -e POSTGRES_PASSWORD=pass123 -e POSTGRES_USER=user123 postgres
```

To access the docker DB.

```bash
docker exec -it champ bash

```

Add authentication logic

```bash
mix phx.gen.auth
```

Add dependencies and make migrations

```bash
mix deps.get
```

```bash
mix ecto.migrate
```

Say you messed up your mix phx.gen.auth and created a table called userss, you could easily undo the error with mix 
```bash
ecto.rollback.
```