# django-cli-no-admin

> Use the Django CLI using "django" without typing "django-admin".

django-cli-no-admin is a config-only project that creates a `django` command and nothing more. With this package, you can use the `django` command instead of `django-admin` to execute management commands in your Django project.

> [!NOTE]
> This package will eventually become unnecessary once [DEP 16](https://github.com/django/deps/blob/main/accepted/0016-name-main-command-django.rst) is fully implemented in Django core. DEP 16 proposes renaming the main Django command from `django-admin` to `django`. Track the implementation progress in [django/deps#100](https://github.com/django/deps/pull/100).

See the blog post: https://micro.webology.dev/2024/12/14/new-project-to.html 

## Installation

You can install django-cli-no-admin using pip:

```shell
pip install django-cli-no-admin
```

Or, if you prefer uv: 

```shell
uv pip install django-cli-no-admin
```

## Usage

Once installed, you can use `django` from the command line in place of `django-admin`:

```shell
django startproject myproject
```

Or any other Django admin command:

```shell
django startapp myapp
```

### Running Project-Specific Commands

By default, the `django` command works with Django's built-in admin commands (like `startproject`, `startapp`, etc.). To run project-specific management commands from your `manage.py` (like `runserver`, `migrate`, `makemigrations`, etc.), you'll need to set the `DJANGO_SETTINGS_MODULE` environment variable:

```shell
export DJANGO_SETTINGS_MODULE=myproject.settings
django runserver
```

Or set it inline:

```shell
DJANGO_SETTINGS_MODULE=myproject.settings django migrate
```

This tells Django where to find your project's settings, allowing you to access all the commands that would normally be available through `manage.py`.

## No Additional Setup Required

There are no additional dependencies or configurations needed. Simply install the package, and you're ready to go. If you need to run project-specific commands, just remember to set `DJANGO_SETTINGS_MODULE` as shown above.

## License

django-cli-no-admin is licensed under the BSD License. See the LICENSE.txt file for details.
