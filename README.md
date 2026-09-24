# PathDoctor

PathDoctor is a lightweight command-line tool designed to help developers diagnose problems with their local development environment. Its main goal is to make common configuration issues easier to understand, especially problems involving PATH, multiple software installations, and tools that are using different versions of the same runtime.

For example, a developer may install a Python package successfully with `pip`, but Python may still report that the package cannot be found. One possible reason is that `pip` and `python` belong to different Python installations. Finding this problem manually can require several terminal commands and can be confusing for developers who are not familiar with environment configuration.

PathDoctor aims to collect this information automatically and explain possible conflicts in a clear way.

## Why PathDoctor?

Development environments can become complicated when multiple versions of Python, Node.js, Java, or other tools are installed on the same computer. Environment variables such as `PATH` determine which executable is used when a command is entered, but it is often difficult to know which version is actually being selected.

PathDoctor is intended to reduce this confusion by showing developers what tools are installed, where they are located, and whether related tools appear to be using different environments.

Instead of only reporting that something is wrong, the project aims to explain why the problem may be happening.

## Planned Features

The first version of PathDoctor will focus on Python development environments.

Planned checks include:

- Detect the location of `python` and `python3`
- Detect the location of `pip` and `pip3`
- Compare the Python installation used by Python and pip
- Display the current PATH entries
- Detect duplicate PATH entries
- Detect PATH entries that no longer exist
- Detect whether a Python virtual environment is active
- Provide simple explanations when a possible configuration problem is found

Future versions may add support for other development tools such as Node.js, npm, Java, Git, Conda, and C/C++ compilers.

## Installation

PathDoctor is currently in the early development stage and is not yet available as an installable package.

When the first working version is released, the project is expected to support installation through Python. The exact installation command will be documented here once the package is available.

For development, contributors will be able to clone the repository:

```bash
git clone https://github.com/NAU-OSS/PathDoctor.git
cd PathDoctor
## Planned Usage

The intended interface is a simple command-line interface.

For example:

```bash
pathdoctor python
```

A future version may produce output similar to:

```text
PathDoctor - Python Environment Diagnosis

Python:
  /opt/homebrew/bin/python3
  Version: 3.12

pip:
  /usr/local/bin/pip3
  Python version: 3.11

Warning:
Python and pip appear to use different Python installations.

Suggestion:
Try installing packages with:

python3 -m pip install <package>
```

The goal is to make the output understandable even for developers who do not have much experience configuring development environments.

Another planned command is:

```bash
pathdoctor path
```

This command would inspect the user's PATH and report possible problems such as duplicate or invalid directories.

## Project Status

PathDoctor is currently in the planning and early development stage.

The project idea, scope, license, and documentation are being established before the first implementation is released. The first goal is to create a small but functional Python environment diagnostic tool before expanding support to additional development environments.

## Roadmap

### Version 0.1

- Read and display PATH information
- Locate Python and pip executables
- Compare Python and pip installations
- Detect common Python environment conflicts

### Version 0.2

- Detect duplicate and invalid PATH entries
- Improve diagnostic messages
- Add automated tests

### Version 0.3

- Add virtual environment and Conda detection
- Add support for macOS, Linux, and Windows differences

### Future

- Node.js and npm diagnostics
- Java and JAVA_HOME diagnostics
- Git configuration checks
- C/C++ compiler detection
- Additional community-contributed environment checks

The roadmap may change as the project develops and contributors provide feedback.

## Contributing

Contributions will be welcome as PathDoctor develops.

Possible contributions include reporting environment problems that PathDoctor should detect, improving diagnostic messages, adding support for additional operating systems and development tools, writing tests, and improving documentation.

More detailed contribution instructions will be provided in the project's `CONTRIBUTING.md` file.

## Community and Support

Questions, bug reports, feature suggestions, and other discussions can be submitted through the GitHub Issues page of this repository.

Using public GitHub Issues will help keep discussions visible so that other users and contributors can learn from previous questions and participate in the project.

Repository:

https://github.com/NAU-OSS/PathDoctor

## License

PathDoctor is released under the MIT License. See `license.md` for the full license text.
