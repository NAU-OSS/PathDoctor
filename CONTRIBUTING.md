# Contributing to PathDoctor

Thank you for your interest in contributing to PathDoctor. The goal of this project is to build a simple and useful command-line tool that helps developers understand and diagnose problems in their local development environments.

PathDoctor is still in an early stage, so contributions can include not only code, but also bug reports, feature ideas, documentation improvements, test cases, and examples of real environment problems.

## How to Contribute

There are several ways to contribute to PathDoctor:

- Report a bug or unexpected behavior
- Suggest a new feature or diagnostic check
- Improve documentation
- Add or improve tests
- Improve existing diagnostic messages
- Add support for another operating system or development tool

For small changes, you may create a branch, make the change, and submit a pull request.

For larger changes, please open an issue first so the idea can be discussed before significant work is started.

A typical contribution process is:

1. Fork or clone the repository.
2. Create a new branch for your change.
3. Make and test your changes.
4. Commit your work with a clear commit message.
5. Push your branch to GitHub.
6. Open a pull request explaining what you changed and why.

## Code Style and Formatting

PathDoctor is primarily a Python project.

Please follow these basic style guidelines:

- Follow Python PEP 8 conventions when possible.
- Use four spaces for indentation.
- Use clear and descriptive variable and function names.
- Keep functions focused on one clear responsibility.
- Avoid unnecessary complexity.
- Add comments when the purpose of the code may not be obvious.
- Keep user-facing diagnostic messages simple and easy to understand.

For example, a message such as:

```text
Warning: pip and Python appear to use different installations.
```

is preferred over a message that only displays raw system information without explaining what may be wrong.

## Testing Requirements

New functionality should be tested before a pull request is submitted.

As the project develops, automated tests will be added for important diagnostic functions. Contributors adding new checks should also add test cases when possible.

Tests should cover:

- Normal expected behavior
- Common incorrect configurations
- Edge cases when information is missing
- Situations where a diagnostic warning should not be produced

Changes should not break existing tests.

If a feature depends on a specific operating system or development environment, please explain how the feature was tested in the pull request.

## Documentation Standards

Documentation is an important part of PathDoctor because the project is intended to help developers understand environment problems.

When adding or changing a feature:

- Update the README if the feature changes installation or usage.
- Explain new commands or options clearly.
- Include a simple example when possible.
- Avoid assuming that readers already understand advanced environment configuration.
- Keep documentation concise and easy to follow.

If you add a new diagnostic check, describe what problem it detects and why the warning is useful.

## Reporting Bugs

Bug reports should be submitted through GitHub Issues.

Before creating a new issue, please check whether a similar issue already exists.

A useful bug report should include:

- A short description of the problem
- Your operating system
- Your Python version
- The command you ran
- The output you expected
- The output you actually received
- Any error messages that appeared

Please remove passwords, API keys, tokens, or other sensitive information before posting logs or environment details.

## Proposing New Features

Feature suggestions are welcome and should also be submitted through GitHub Issues.

When proposing a feature, please explain:

- What problem the feature would solve
- Who would benefit from it
- An example of how it might work
- Whether it applies to a specific operating system or development tool

Examples of possible future contributions include support for Node.js, npm, Java, Conda, Git, and C/C++ development environments.

Small and beginner-friendly ideas may be labeled as `good first issue` to make it easier for new contributors to participate.

## Community Guidelines

Contributors are expected to communicate respectfully and constructively.

Please:

- Be respectful of different experience levels and backgrounds.
- Give constructive feedback.
- Focus discussions on the technical problem rather than the person.
- Be patient with new contributors.
- Ask questions when requirements are unclear.
- Accept that not every proposed feature will fit the scope of the project.

The goal is to make PathDoctor a project where people feel comfortable asking questions, suggesting ideas, and learning from each other.

A separate `CODE_OF_CONDUCT.md` will provide additional community expectations.

## Questions

If you are unsure how to contribute, open a GitHub Issue and describe what you would like to work on.

Thank you for helping improve PathDoctor.
