# Heroku buildpack to which installs cloudflared

This is a Heroku buildpack that makes `cloudflared` available to your heroko dyno.


### Usage

Once this buildpack is added you can create a `.profile` in the root of your app which sets up any tunnels you'd like

As an example you can add a line like this to setup a local tunnel to a database server which is configured to tunnel via cloudflare access.
```
cloudflared access tcp --hostname db.example.com --url localhost:1433 &
```
