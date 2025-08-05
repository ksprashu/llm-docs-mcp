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

To get started with the `llms-docs-mcp`, you can clone the repository directly into your Gemini CLI extensions directory. You have the option of a global installation, which will be available to your user everywhere, or a local installation for the current workspace.

### Prerequisites

- **Gemini CLI**: Ensure you have the Gemini CLI installed and configured on your system.

### Clone the Repository

#### Global Installation
```bash
mkdir -p ~/.gemini/extensions
git clone https://github.com/google/llms-docs-mcp.git ~/.gemini/extensions/llms-docs-mcp
```

#### Workspace Installation
```bash
mkdir -p ./.gemini/extensions
git clone https://github.com/google/llms-docs-mcp.git ./.gemini/extensions/llms-docs-mcp
```

### Install Dependencies

The `llms-docs-mcp` extension is designed to be self-contained and does not require any additional dependencies to be installed. Once cloned into the appropriate directory, the Gemini CLI will automatically load the extension on startup.

### Configure Environment

The `llms-docs-mcp` uses a `config.json` file to manage documentation sources. This file is located in the `llms-docs-mcp/` directory and can be customized to add, update, or remove documentation sources as needed.

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