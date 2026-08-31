# simple-ldap-login

A simple way to authenticate to your WordPress site using LDAP. It's a fork of [clifgriffin/simple-ldap-login](https://github.com/clifgriffin/simple-ldap-login) with some improvements.

## Features

* Supports Active Directory and OpenLDAP (and other directory systems which comply to the LDAP standard, such as OpenDS)
* Supports TLS
* Uses up-to-date methods for WordPress authentication routines.
* Authenticates existing WordPress usernames against LDAP.
* Can be configured to automatically create WordPress users for valid LDAP logins.
* You can restrict logins based on one or more LDAP groups.
* Intuitive control panel.

## Installation

1. Use the WordPress plugin directory to install the plugin or upload the directory `simple-ldap-login` to the `/wp-content/plugins/` directory.
1. Activate the plugin through the 'Plugins' menu in WordPress
1. Update the settings to those that best match your environment by going to Settings -> Simple LDAP Login
1. If you don't get the settings right the first time, don't fret! Just use your WordPress credentials. They should always work
1. Once you have the settings correct, you can toggle LDAP Exclusive mode (if you like).
1. To make your life easier, consider using two different browsers (e.g., Chrome and Firefox) to do testing.  Change settings in one. Test in the other. This will prevent any chance of being locked out.

## Development environment

### Basic commands

```bash
# Install dependencies
composer install
```

### Lando

We use Lando to create a WP installation to test this plugin. You can find the instructions to install it [here](https://docs.lando.dev/basics/installation.html).

Once you have Lando installed, you can run the following commands to start the development environment:

```bash
# Start the development environment
# username: admin
# password: password
lando start

# Reset the development environment
lando destroy && rm -rf wp-www

# Destroy the lando containers
lando poweroff
```

## Changelog

See [readme.txt](readme.txt) for the full changelog.
