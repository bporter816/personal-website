# personal-website

The source for <https://bporter.net>.

Styled with [Bulma](https://bulma.io), built with [Hugo](https://gohugo.io), and deployed to
[Cloudflare Workers](https://workers.cloudflare.com).

`build.sh` is the entrypoint for building the site. It runs `spotify.py` and `steam.py` to get data about my recent
music and games from the Spotify and Steam APIs. The responses are placed in the `data/` directory and injected into the
layouts.

The dynamic content is updated by a deploy hook called by a scheduled Worker that runs daily.
