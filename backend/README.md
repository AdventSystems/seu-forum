## Guia de Configuração

-   Adicione um arquivo .env no root do backend com as configurações do .env.example
-   Gere uma api key
-   Rode o comando de Alias do Sail

```bash
alias sail='sh $([ -f sail ] && echo sail || echo vendor/bin/sail)'
```

-   Instale as dependências do composer

```bash
docker run --rm \
    -u "$(id -u):$(id -g)" \
    -v "$(pwd):/var/www/html" \
    -w /var/www/html \
    laravelsail/php83-composer:latest \
    composer install --ignore-platform-reqs
```

-   Rode o docker

```bash
sail up -d
```

-   Rode os migrations

```bash
sail artisan migrate
```

## Comandos

Rodar o docker

```bash
sail up -d
```

Parar o docker

```bash
sail down
```

Rodar migrations

```bash
sail artisan migrate
```

Criar migrations

```bash
sail artisan make:migration
```
