# Rumbrella

This is an Elixir/Phoenix umbrella app containing a web app called Rumblr and a
separate service called Info_sys which calls the public Wolfram API. These were created
by following along with the Programming Phoenix book.

Not included in the how to below is adding a Wolfram developer key to the app config.
this could be added to `apps\rumbl\config\dev.secret.exs`:
    
    use Mix.Config
    config :info_sys, :wolfram, app_id: "YOUR_KEY"
    
Finally, import to `dev.exs`.

## How to use

1. Clone repo
2. Install dependencies `mix deps.get`
3. Create and migrate db with `ix ecto.create && ecto.migrate`
4. Install Node.js dependencies with `npm install`
5. Start project with `mix phoenix.server`
6. Visit at localhost:4000

* All at once: `mix deps.get && mix ecto.create && mix ecto.migrate && npm install && mix phoenix.server`