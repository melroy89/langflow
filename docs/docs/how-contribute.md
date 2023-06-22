# How to contribute?

👋 Hello there! We welcome contributions from developers of all levels to our open-source project on [GitHub](https://github.com/logspace-ai/langflow). If you'd like to contribute, please check our contributing guidelines and help make LangFlow more accessible.

As an open-source project in a rapidly developing field, we are extremely open
to contributions, whether in the form of a new feature, improved infra, or better documentation.

To contribute to this project, please follow a ["fork and pull request"](https://docs.github.com/en/get-started/quickstart/contributing-to-projects) workflow.

Please do not try to push directly to this repo unless you are a maintainer.

---
## Local development

You can develop LangFlow using docker compose, or locally.

We provide a .vscode/launch.json file for debugging the backend in VSCode, which is a lot faster than using docker compose.

Setting up hooks:
```bash
make init
```

This will install the pre-commit hooks, which will run `make format` on every commit.

It is advised to run `make lint` before pushing to the repository.

---

## Run locally

LangFlow can run locally by cloning the repository and installing the dependencies. We recommend using a virtual environment to isolate the dependencies from your system.

Before you start, make sure you have the following installed:

- Poetry
- Node.js

Then install the dependencies and start the development server for the backend:

```bash
poetry install
make backend
```

And the frontend:

```bash
make frontend
```

---

## Docker compose

The following snippet will run the backend and frontend in separate containers. The frontend will be available at `localhost:3000` and the backend at `localhost:7860`.

```bash
docker compose up --build
# or
make dev build=1
```