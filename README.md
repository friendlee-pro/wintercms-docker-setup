# WinterCMS installation with Docker 

- `git clone git@github.com:friendlee-digital/wintercms-docker-setup.git <your-winter-instance>`
- `cd <your-winter-instance>`
- `git clone --branch v1.2.1 --depth 1 git@github.com:wintercms/winter.git html`
- `cd html && rm -rf .github .gitpod .vscode .gitpod.yml .git CHANGELOG.md README.md && cd ..`
  
  Clean redundant stuff + `.git` folder so you can use your remote origin
- `docker compose build`
- `docker compose up -d`
- `docker compose exec winter composer install`
- `docker compose exec winter php artisan winter:install`
  
  Here remember to use `db` as `MySQL Host`.

#### Additional resources
- https://www.digitalocean.com/community/tutorials/how-to-install-and-set-up-laravel-with-docker-compose-on-ubuntu-22-04
