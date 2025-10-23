> [!WARNING]
> **This repository is no longer maintained by our internal teams.**  
> The template is provided *as is* and will not receive updates, bug fixes, or new features.  
> You are welcome to contribute on it or fork the repository and modify it for your own use.
> To deploy this template on [Upsun](https://www.upsun.com), you can use the command [upsun project:convert](https://docs.upsun.com/administration/cli/reference.html#projectconvert)
> on this codebase to convert the existing `.platform.app.yaml` configuration file to the [Upsun Flex format](https://docs.upsun.com/create-apps/app-reference/single-runtime-image.html).

# Django 3 for Platform.sh

This template deploys the Django 3 application framework on Platform.sh, using the gunicorn application runner.  It also includes a PostgreSQL database connection pre-configured.

Django is a Python-based web application framework with a built-in ORM.

## Features

* Python 3.8
* PostgreSQL 12
* Automatic TLS certificates
* Pipfile-based build

## Customizations

The following files have been added to a basic Django configuration.  If using this project as a reference for your own existing project, replicate the changes below to your project.

* The `.platform.app.yaml`, `.platform/services.yaml`, and `.platform/routes.yaml` files have been added.  These provide Platform.sh-specific configuration and are present in all projects on Platform.sh.  You may customize them as you see fit.
* An additional Pip library, [`platformshconfig`](https://github.com/platformsh/config-reader-python), has been added.  It provides convenience wrappers for accessing the Platform.sh environment variables.
* A rudimentary `myapp` application is included for demonstration purposes.  In particular, the `settings.py` file is set up to configure Django to connect to the correct database, and run in Debug mode when not running the `master` branch.  You are free to change that configuration if you prefer.

## References

* [Django](https://www.djangoproject.com/)
* [Python on Platform.sh](https://docs.platform.sh/languages/python.html)
