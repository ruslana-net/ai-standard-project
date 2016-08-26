# Symfony 2.8 + Sonata Admin Standard Project

## Install

### 1 Create DB
```sh
echo "CREATE DATABASE db_name CHARACTER SET utf8 COLLATE utf8_general_ci;" | mysql -u username -p
```

### 2 Init
```sh
cd /path/to/project
git clone git@github.com:ruslana-net/ai-standard-project.git ./
composer install
cp web/.htaccess.dist web/.htaccess
```

## 3. Run
```bash
php app/console doctrine:schema:create
php app/console doctrine:schema:update --force
php app/console assets:install web
php app/console cache:clear
```

## 4. Add admin users
```bash
php app/console fos:user:create
php app/console fos:user:promote admin ROLE_SONATA_ADMIN
php app/console fos:user:promote admin ROLE_SUPER_ADMIN
```

## Git

### 1 Remove old remote
```sh
git remote remove origin
```

### 2 Create repository and add new remote
```sh
git remote add origin ...
```