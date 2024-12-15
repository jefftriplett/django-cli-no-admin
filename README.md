# django-cli-no-admin

> Use the Django CLI using "django" without typing "django-admin".

django-cli-no-admin is a config-only project that creates a `django` command and nothing more. With this package, you can use the `django` command instead of `django-admin` to execute management commands in your Django project.

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

Or any other Django management command:

```shell
django runserver
```

## No Additional Setup Required

There are no additional dependencies or configurations needed. Simply install the package, and you're ready to go.

## License

django-cli-no-admin is licensed under the BSD License. See the LICENSE.txt file for details.
