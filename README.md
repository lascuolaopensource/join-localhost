# Join Localhost
## Local development edition

Gestionale per nuove istituzioni

## Install

Clone repository:
        
        git clone https://github.com/lascuolaopensource/join-localhost.git
        cd join-localhost

### Set variables

Rename `env-example` to `.env` in main folder, `join-frontend` and `join-admin-frontend`:

        mv env-example .env
        mv join-frontend/env-example join-frontend/.env
        mv join-frontend/env-example join-admin-frontend/.env

If you want to change addresses or ports check out variables in those files. Be sure to match 'em in `docker-compose.yml` too.

### Hosts file

You need to add these lines to your `hosts` file:

        127.0.0.1 frontend
        127.0.0.1 admin-frontend
        127.0.0.1 backend

On Linux and Mac you can find it in `/etc/hosts`.

On Windows you can find it in `C:\Windows\System32\drivers\etc\hosts`.

### Build
        
Then take everything up with:

        docker-compose up
        
### Check
Then you can check your [public-frontend](http://frontend:1234) and [admin-frontend](http://admin-frontend:1235).
