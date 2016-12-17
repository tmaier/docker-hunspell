# Docker image for hunspell

This is a lightweight docker image for [hunspell](http://hunspell.github.io).
Hunspell is spell checker.
See http://hunspell.github.io

The working directory is at `/workdir`. Mount your volume into that directory.

```bash
$ docker run -ti -v $(pwd):/workdir tmaier/hunspell:latest -H "public/**/*.html"
```

## Other languages

List all languages available:

```bash
docker run -ti tmaier/hunspell -D
```

Example:

```bash
$ docker run -ti -v $(pwd):/workdir tmaier/hunspell -u3 -i utf-8 -d de_DE_neu,en_US -p words -H "public/**/*.html"
```

## Continuous Integration (CI)

Run in report mode

```bash
$ docker run -ti -v $(pwd):/workdir tmaier/hunspell -u3 -H "public/**/*.html"
```

## Author

[Tobias L. Maier](http://tobiasmaier.info) for [BauCloud GmbH](http://www.baucloud.com)
