<p align="center">
    <a href="https://sylius.com" target="_blank">
        <img src="https://demo.sylius.com/assets/shop/img/logo.png" />
    </a>
</p>

[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/JoppeDC/SyliusBetterSeoPlugin/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/JoppeDC/SyliusBetterSeoPlugin/?branch=master)
[![Build Status](https://scrutinizer-ci.com/g/JoppeDC/SyliusBetterSeoPlugin/badges/build.png?b=master)](https://scrutinizer-ci.com/g/JoppeDC/SyliusBetterSeoPlugin/build-status/master)

<h1 align="center">WIP: Sylius Better SEO Plugin</h1>
    
<p align="center">
  Adding customizable SEO meta tags and Google structured data to product pages.
</p>
  
<img src="https://imgur.com/wTZtSDa.jpg" alt="Kitten" title="Google Preview" height="150" >
<img src="https://imgur.com/wvLt5em.jpg" alt="Kitten" title="Facebook Preview" height="150" >
<img src="https://imgur.com/hMNvu2C.jpg" alt="Kitten" title="Twitter Preview" height="150" >

## Local Development Test

1. Clone the repo to a local folder and install composer dependencies using the following command:
    ```
    $ composer install
    ```

2. From the plugin root directory, run the following commands:

    ```bash
    $ (cd tests/Application && yarn install)
    $ (cd tests/Application && yarn build)
    $ (cd tests/Application && bin/console assets:install public -e test)
    
    $ (cd tests/Application && bin/console doctrine:database:create -e test)
    $ (cd tests/Application && bin/console doctrine:schema:create -e test)
    ```

In this case i used a docker-compose database. You can use your own database, but don't forget to set the credentials in the .env file.

### Opening Sylius with the plugin

- Using `dev` environment:

    ```bash
    $ (cd tests/Application && bin/console sylius:fixtures:load -e dev)
    $ (cd tests/Application && bin/console server:run -d public -e dev)
    ```
