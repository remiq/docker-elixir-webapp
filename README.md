# docker-elixir-webapp

This project shows an example of creating Elixir web application using docker containers.

mix archive.install https://github.com/phoenixframework/phoenix/releases/download/v0.11.0/phoenix_new-0.11.0.ez

# On developers machine (compiling)

    MIX_ENV=prod mix compile.protocols

## On docker container (running)

    cd /app/web
    mix deps.get
    MIX_ENV=prod PORT=4001 elixir -pa _build/prod/consolidated -S mix phoenix.server

