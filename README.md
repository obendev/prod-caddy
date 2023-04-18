# prod-caddy
A production-ready Caddyfile, probably

This project is inspired by [h5bp/server-configs-apache](https://github.com/h5bp/server-configs-apache) and [h5bp/server-configs-nginx](https://github.com/h5bp/server-configs-nginx).  
I'd like to to provide a ready to go Caddy configuration, in form of a [Caddyfile](https://caddyserver.com/docs/quick-starts/caddyfile).

## Getting started
Before using this configuration snippet, please make sure you're familiar with how to use a `Caddyfile`.  
I strongly recommend that you at least read the Getting Started Guide of Caddy, [Getting Started — Caddy Documentation (caddyserver.com)](https://caddyserver.com/docs/getting-started).

### Caddy structure
The Caddyfile's structure can be described visually:
![Visualized Caddy structure](https://caddyserver.com/resources/images/caddyfile-visual.png)

Further information can be found here: [Caddyfile Concepts — Caddy Documentation (caddyserver.com)](https://caddyserver.com/docs/caddyfile/concepts)

### PHP support
By default, PHP support isn't implemented in this Caddyfile, due to different use-cases among users.
If you'd like to implement PHP support, please refer to [Common Caddyfile Patterns — Caddy Documentation (caddyserver.com)](https://caddyserver.com/docs/caddyfile/patterns#php)
Here is a sample snippet you could implement:
```
(php82) {
        encode gzip
        php_fastcgi unix//run/php/php8.2-fpm.sock
}
```
