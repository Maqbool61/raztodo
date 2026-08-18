# Contributing to RazTodo

Thanks for wanting to help with RazTodo. Whatever your experience level, there are different ways to help, from small fixes and documentation improvements to more involved changes. You don't need permission or deep knowledge of the codebase to get started, just pick something that interests you and go.

## Picking an Issue 🔎

Just browse the [open issues](https://github.com/razbuild/raztodo/issues) and grab whatever catches your eye. Keep an eye on the labels, they can give you a hint about how big or tricky something is, but don't overthink it. If it looks fun, go for it.

## How to Get Started 🚀

1. Pick an issue.
2. Comment on it to say you're picking it up.
3. Create a branch from the repository (fork if you don't have write access).
4. Make your change.
5. Run the tests and quality checks (commands below).
6. Open a Pull Request.

> 💬 **Questions? Just ask.** Issue confusing, or already picked by someone else? Say so in the comments and grab another one. We'd much rather you ask than get stuck.

## Before You Start 📝

* Check existing issues before opening a new one.
* Use the provided issue templates.
* Keep discussions respectful and constructive.

Please follow our [Code of Conduct](https://github.com/razbuild/.github/blob/main/CODE_OF_CONDUCT.md).

## Early Feedback 🌱

RazTodo is still an early project, so feedback is especially valuable.

You don't need to be a developer to help. If you try RazTodo and notice
something confusing, broken, or missing, we'd love to hear about it.

Share your experience in the
[Early Feedback discussion](https://github.com/razbuild/raztodo/discussions).

Things that are useful to us:

- CLI experience
- Web UI experience
- Installation and setup
- Documentation
- Bugs or confusing behavior
- Features you'd expect from a task manager

Even a few notes after trying the project are helpful.

## Reporting Bugs 🐛

Please include:

* RazTodo version
* Operating system
* Python version
* Steps to reproduce
* Expected behavior
* Actual behavior

## Development Setup 🛠️

You just need Python 3.10+ and [`uv`](https://docs.astral.sh/uv/). Then:

```bash
git clone https://github.com/razbuild/raztodo.git
cd raztodo
uv sync --editable --group dev --extra web
```

That's it, you're ready. Curious how the project is put together? Check [`docs/ARCHITECTURE.md`](docs/ARCHITECTURE.md).

## Running Tests 🧪

```bash
uv run pytest -v
```

Run a single file or test:

```bash
uv run pytest tests/application/use_cases/test_create_task.py
uv run pytest tests/application/use_cases/test_create_task.py::TestCreateTaskUseCase::test_create_task_success
```

Check coverage:

```bash
uv run coverage run -m pytest
uv run coverage report -m
```

More detail in [`docs/TESTING.md`](docs/TESTING.md).

## Code Quality ✨

Before opening a PR, run:

```bash
uv run ruff format src/ tests/
uv run ruff check --fix src/ tests/
uv run ty check src/
```

These are the same checks CI runs, so passing them locally saves a round trip. Also add tests for new functionality, and update docs when behavior changes.

## Commit Messages

Use conventional prefixes:

* `feat:` New features
* `fix:` Bug fixes
* `docs:` Documentation
* `test:` Tests
* `refactor:` Refactoring
* `chore:` Maintenance

Example:

```text
feat: add local model discovery
fix: handle invalid configuration file
```

## Branch Naming

Use clear branch names that describe the change you're making. Prefer short names with a category prefix:

* `feat/` New features
* `fix/` Bug fixes
* `docs/` Documentation changes
* `test/` Test changes
* `refactor/` Code improvements without behavior changes
* `chore/` Maintenance tasks

Examples:

```text
feat/add-task-filters
fix/handle-empty-config
docs/update-contributing-guide
test/add-task-validation-tests
refactor/simplify-task-service
```

## Pull Requests

A good PR description includes:

* What problem it solves
* How it solves it
* What you tested, and how
* Screenshots, for Web UI changes
* Any related documentation updates

Keep it short and clear, no need to over-explain.

## What Happens After I Open a PR?

A maintainer will review it and may request changes. Update your PR based on feedback, and it’ll be merged once approved.

## Keep Going 🔁

Merged your first PR? Grab [another one](https://github.com/razbuild/raztodo/issues). You already know your way around now, we'd love to see you back.