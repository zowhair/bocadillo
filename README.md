<p align="center">
    <img src="https://github.com/bocadilloproject/bocadillo/blob/master/.github/banner.png?raw=true">
</p>

---

[![python](https://img.shields.io/pypi/pyversions/bocadillo.svg?logo=python&logoColor=fed749&colorB=3770a0&label=)](https://www.python.org)
[![pypi](https://img.shields.io/pypi/v/bocadillo.svg)][pypi-url]
[![travis](https://img.shields.io/travis/bocadilloproject/bocadillo.svg)](https://travis-ci.org/bocadilloproject/bocadillo)
[![black](https://img.shields.io/badge/code_style-black-000000.svg)](https://github.com/ambv/black)
[![codecov](https://codecov.io/gh/bocadilloproject/bocadillo/branch/master/graph/badge.svg)](https://codecov.io/gh/bocadilloproject/bocadillo)
[![license](https://img.shields.io/pypi/l/bocadillo.svg)][pypi-url]
[![Join the chat at https://gitter.im/bocadilloproject/bocadillo](https://badges.gitter.im/bocadilloproject/bocadillo.svg)](https://gitter.im/bocadilloproject/bocadillo)

[pypi-url]: https://pypi.org/project/bocadillo/

[Documentation][docs] / [CLI](https://github.com/bocadilloproject/queso) / [Twitter](https://twitter.com/bocadillopy) / [Blog](https://bocadilloproject.github.io/blog/) / [Mentions](https://bocadilloproject.github.io/mentions.html) / [FAQ](https://bocadilloproject.github.io/faq/)

[docs]: https://bocadilloproject.github.io

> Migrating from v0.13.x? Read the [v0.14 release notes](https://bocadilloproject.github.io/blog/release-0.14.html).

Bocadillo is a **Python async web framework** that makes server-side async web apps **fun to build** and **accessible to everyone**.

It is designed to be:

- **Productive**: a carefully chosen set of included batteries helps you solve common and more advanced problems — request routing, app configuration, static files, data validation, and more!

- **Real-time capable**: embrace asynchronous programming and the baked-in WebSocket and SSE support to build real-time, highly-concurrent systems.

- **Flexible**: inject resources into web views using providers, an explicit, modular and easy-to-use mechanism inspired by pytest fixtures.

- **Performant**: squeeze the juice out of [Starlette] and [uvicorn], the lightning-fast ASGI toolkit and web server.

- **Empowering**: use tailored testing and command line tools to build delicious, high-quality applications.

- **Transparent**: every single feature is documented front to back and has optimal editor support thanks to a 100% type-annotated code base.

[starlette]: https://www.starlette.io
[uvicorn]: https://www.uvicorn.org

## Quick start

We all love delicious "Hello, world!" examples, don't we? Here's ours:

1. Install Bocadillo and the [Bocadillo CLI]:

```bash
pip install bocadillo bocadillo-cli
```

[bocadillo cli]: https://github.com/bocadilloproject/bocadillo-cli

2. Generate the project and `cd` into it:

```bash
bocadillo create hello
cd hello/
```

3. Edit the application script:

```python
# hello/app.py
from bocadillo import App

app = App()

@app.route("/")
async def index(req, res):
    res.text = "Hello, world!"
```

4. Start a [uvicorn] server (hot reload enabled!):

```bash
uvicorn hello.asgi:app --reload
```

5. Say hello!

```bash
$ curl http://localhost:8000
Hello, world!
```

6. Edit `app.py` to send "Hello, Bocadillo!" instead, then hit save. Uvicorn will pick up the changes and restart the application. Try it out again:

```bash
$ curl http://localhost:8000
Hello, Bocadillo!
```

Tastes good! 🥪

Hungry for more? Head to the [docs].

## Changelog

We record changes to Bocadillo in the [changelog](https://github.com/bocadilloproject/bocadillo/blob/master/CHANGELOG.md). In particular, check out the [Unreleased](https://github.com/bocadilloproject/bocadillo/blob/master/CHANGELOG.md#unreleased) section to see what's coming in the next release.

## Contributing

Found a bug? A typo? Want to help build a new feature? We'd love to see your contributions! There are also many ways to contribute that don't include code: helping with issues, laying out new ideas, improving docs, etc.

Check out our [Contributing guide](https://github.com/bocadilloproject/bocadillo/blob/master/CONTRIBUTING.md) to get started.

By the way, here's our Contributor Hall of Fame. 👨‍💻👩‍💻

[![](https://sourcerer.io/fame/florimondmanca/bocadilloproject/bocadillo/images/0)](https://sourcerer.io/fame/florimondmanca/bocadilloproject/bocadillo/links/0)[![](https://sourcerer.io/fame/florimondmanca/bocadilloproject/bocadillo/images/1)](https://sourcerer.io/fame/florimondmanca/bocadilloproject/bocadillo/links/1)[![](https://sourcerer.io/fame/florimondmanca/bocadilloproject/bocadillo/images/2)](https://sourcerer.io/fame/florimondmanca/bocadilloproject/bocadillo/links/2)[![](https://sourcerer.io/fame/florimondmanca/bocadilloproject/bocadillo/images/3)](https://sourcerer.io/fame/florimondmanca/bocadilloproject/bocadillo/links/3)[![](https://sourcerer.io/fame/florimondmanca/bocadilloproject/bocadillo/images/4)](https://sourcerer.io/fame/florimondmanca/bocadilloproject/bocadillo/links/4)[![](https://sourcerer.io/fame/florimondmanca/bocadilloproject/bocadillo/images/5)](https://sourcerer.io/fame/florimondmanca/bocadilloproject/bocadillo/links/5)[![](https://sourcerer.io/fame/florimondmanca/bocadilloproject/bocadillo/images/6)](https://sourcerer.io/fame/florimondmanca/bocadilloproject/bocadillo/links/6)[![](https://sourcerer.io/fame/florimondmanca/bocadilloproject/bocadillo/images/7)](https://sourcerer.io/fame/florimondmanca/bocadilloproject/bocadillo/links/7)

## Credits

Logo designed by Florimond Manca. Sandwich icon designed by [macrovector](http://macrovector.com).
