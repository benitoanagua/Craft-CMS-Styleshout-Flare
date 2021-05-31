# Craft Styleshout Flare

This repo contains  the template [Styleshout Flare](https://www.styleshout.com/free-templates/flare/), front-end resources, and a MySQL database backup, a Craft demo site.

You can find out more about Craft at [craftcms.com](https://craftcms.com/).

## Features

This demo takes advantage of several Craft features:

#### Sections
The content in Happy Lager is managed from the following [sections](https://docs.craftcms.com/v3/sections-and-entries.html#sections):

#### Entry Types
The News section has two [entry types](https://docs.craftcms.com/v3/sections-and-entries.html#entry-types):

#### Matrix Fields
This site has the following [Matrix fields](https://docs.craftcms.com/v3/matrix-fields.html):

#### Relations
This site has the following [relational fields](https://docs.craftcms.com/v3/relations.html#terminology):

#### Assets
This site has the following [asset volumes](https://docs.craftcms.com/v3/assets.html):



## Installation

If you want to install the site locally, follow these instructions:

1. Download/clone the repo on your computer:

   ```bash
   https://github.com/benitoanagua/Craft-CMS-Styleshout-Flare.git
   ```

2. Run `composer install` within the clone:

   ```bash
   cd Craft-CMS-Styleshout-Flare
   composer install
   ```

3. Copy the `.env.example` file at the root of the project to `.env`, and set its `DB_SERVER`, `DB_USER`, and `DB_PASSWORD` (`PRIMARY_SITE_URL=http://localhost:3000`)  variables to the correct values.
   ```bash
   cp .env.example .env
   ```

4. Ensure that the following files and directories have permissions that will allow PHP to read and write to them:

   - `.env`
   - `composer.json`
   - `composer.lock`
   - `config/license.key`
   - `storage/*`
   - `vendor/*`
   - `web/cpresources/*`

5. Run this command in the CLI from your project's root to automatically generate a security key for the site: `php craft setup/security-key`

6. Create a new MySQL database called `flare`, and import `flare.sql` into it, something like this.
   ```bash
   mariadb -u root -p flare < flare.sql
   ```

7. Enter the directory and run the internal php web server.

 ```bash
   cd web/
   php -S localhost:3000
   ```

## Logging in

The Craft Control Panel is located at `http://localhost:3000/admin`. You can log in with the following credentials:

* Username: `admin`
* Password: `secret`

