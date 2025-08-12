# llms-docs-mcp

![Build Status](https://img.shields.io/badge/build-passing-brightgreen)
![Version](https://img.shields.io/badge/version-0.1.0-blue)
![License](https://img.shields.io/badge/license-Apache--2.0-blue)

## Description

The `llms-docs-mcp` is a sophisticated, documentation-aware extension for the Gemini CLI, designed to provide developers with the most current and accurate information about various libraries and frameworks. By dynamically fetching and referencing official documentation, this tool ensures that all responses are based on the latest updates, rather than on potentially outdated internal knowledge.

At its core, the `llms-docs-mcp` runs a local MCP (Model Context Protocol) server that provides documentation context directly to the Gemini model. This allows the system to be highly extensible, with a simple yet powerful `config.json` file for managing multiple documentation sources. With this extension, developers can rapidly expand the CLI's knowledge base, ensuring that it remains a reliable and up-to-date resource for all their development needs.

## Key Features

- **Extensible Documentation Sources**: Easily add, update, or remove documentation sources through a centralized `config.json` file, ensuring the system can adapt to new libraries and frameworks.
- **Automated Integration Workflow**: A semi-automated workflow allows for the rapid and accurate integration of new documentation sources, minimizing manual effort and ensuring consistency.
- **Up-to-Date and Accurate Information**: By fetching documentation directly from official sources, the extension provides the most reliable and current information, avoiding the pitfalls of outdated knowledge.
- **Seamless Gemini CLI Integration**: The extension integrates smoothly with the Gemini CLI, with automatic loading at startup for both global and workspace installations.
- **High-Quality, Professional Standard**: The `llms-docs-mcp` is designed to meet the highest standards of professional development, with a well-structured, intuitive, and user-friendly interface.

## Tech Stack

- **Gemini CLI**: The extension is built to integrate seamlessly with the Gemini CLI, enhancing its capabilities with documentation-aware features.
- **MCP (Model Context Protocol)**: A local MCP server provides the documentation context directly to the Gemini model, ensuring real-time, accurate information.
- **JSON**: A `config.json` file is used to manage and configure the documentation sources, allowing for easy customization and extensibility.
- **Shell Scripting**: The extension leverages shell scripting for automated workflows and seamless integration with the command-line interface.

## Installation and Setup

To get started with the `llms-docs-mcp`, clone the repository to a location of your choice and then create a symbolic link to it from the Gemini CLI extensions directory. This is the recommended setup for development, as it ensures any changes you make are immediately reflected in the CLI.

### Prerequisites

- **Gemini CLI**: Ensure you have the Gemini CLI installed and configured on your system.
- **Git**: Ensure you have Git installed.
- **Python and Pip**: This extension requires Python 3.8 or higher. You can download it from [python.org](https://www.python.org/downloads/). Pip, the package installer for Python, is included with modern Python versions.
- **uv**: This extension uses `uv` to manage Python packages and environments. Once you have Python and pip installed, you can install `uv` by running the following command in your terminal:
  ```bash
  pip install uv
  ```

### 1. Clone the Repository

First, clone the repository to your local machine.

```bash
git clone https://github.com/ksprashu/llm-docs-mcp.git
cd llm-docs-mcp
```

### 2. Create a Symbolic Link

Next, create a symbolic link from the `llms-docs-mcp` subdirectory to the Gemini CLI's global extensions folder. This allows the CLI to discover and load the extension automatically.

```bash
# Get the absolute path to the current directory
SOURCE_DIR="$(pwd)/llms-docs-mcp"

# Define the destination directory for Gemini extensions
DEST_DIR="$HOME/.gemini/extensions/llms-docs-mcp"

# Create the extensions directory if it doesn't exist
mkdir -p "$HOME/.gemini/extensions"

# Create the symbolic link
ln -s "$SOURCE_DIR" "$DEST_DIR"

echo "Successfully created symlink. The llms-docs-mcp extension is now installed."
```

The Gemini CLI will now load the extension on startup. Any updates you pull from the Git repository will be available immediately.

### Alternative: Manual Installation

If you prefer not to use a symbolic link, you can manually copy the `llms-docs-mcp` directory into the Gemini extensions folder.

#### Global Installation
```bash
mkdir -p ~/.gemini/extensions
cp -R llms-docs-mcp ~/.gemini/extensions/
```

#### Workspace Installation
```bash
mkdir -p ./.gemini/extensions
cp -R llms-docs-mcp ./.gemini/extensions/
```

Note that with this method, you will need to manually copy the folder again every time you want to update the extension.


## Usage

The `llms-docs-mcp` is designed to be used directly through the Gemini CLI. Once installed, the extension will automatically provide documentation-aware responses to your queries. To add a new documentation source, you can use the following command format:

```
Add a new documentation source: [Name of Source] from [URL to llms.txt]
```

For example, to add the documentation for a new library called "SuperLib", you would use the following prompt:

```
Add a new documentation source: SuperLib from https://superlib.com/docs/llms.txt
```

The extension will then guide you through the process of integrating the new documentation source.

## Running Tests

Currently, the `llms-docs-mcp` does not include a dedicated test suite. However, you can verify that the extension is working correctly by running a query related to one of the configured documentation sources and ensuring that the response is accurate and up-to-date.

## Contributing

Contributions are welcome! If you would like to contribute to the `llms-docs-mcp`, please follow these steps:

1.  **Fork the repository**: Create a fork of the repository to your own GitHub account.
2.  **Create a branch**: Create a new branch for your changes.
3.  **Make your changes**: Implement your changes, ensuring they are consistent with the project's standards.
4.  **Submit a pull request**: Submit a pull request with a clear description of your changes.

We appreciate your contributions and will review your pull request as soon as possible.

## License

This project is licensed under the Apache License, Version 2.0. For more information, please see the [LICENSE](LICENSE) file.