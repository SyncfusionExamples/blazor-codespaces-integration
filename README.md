# Blazor Codespaces Integration

This repository contains a Blazor Web App with Interactive Server rendering, integrated with the [Blazor DataGrid](https://www.syncfusion.com/blazor-components/blazor-datagrid), and configured to run in [GitHub Codespaces](https://docs.github.com/en/codespaces/about-codespaces) by using a development container.

It enables a cloud-based development experience without requiring a local environment setup.

## Features

- Blazor Web App with Interactive Server rendering
- [Blazor DataGrid](https://www.syncfusion.com/blazor-components/blazor-datagrid) integration
- Preconfigured `.devcontainer` for Codespaces
- [.NET 10 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/10.0) environment
- Automatic dependency restoration and setup
- Ready-to-run sample with minimal configuration

## Prerequisites

Before getting started, ensure you have the following:

- A [GitHub](https://github.com/) account
- Access to [GitHub Codespaces](https://docs.github.com/en/codespaces/about-codespaces)

## Dev container configuration

This repository already includes a preconfigured development container at:

`.devcontainer/devcontainer.json`

### Key configuration details

- Base image uses the official .NET 10 development container image
- Includes [GitHub CLI](https://cli.github.com/) support
- Installs required Visual Studio Code extensions for Blazor and C#
- Configures port forwarding for the application on port 5000
- Installs WebAssembly (WASM) tools automatically
- Restores NuGet packages during container setup

This setup ensures that the development environment is ready immediately after Codespaces starts.

## Running the application in GitHub Codespaces

Follow these steps to run the application:

### 1. Open the repository

Open this repository in your browser on GitHub.

### 2. Launch Codespaces

- Click the **Code** button
- Select the **Codespaces** tab
- Click **Create codespace on main**

### 3. Wait for initialization

GitHub Codespaces will automatically:

- Create the development container
- Install the .NET SDK and required tools
- Restore dependencies
- Open Visual Studio Code in the browser

### 4. Run the application

Once Codespaces is ready, open the integrated terminal and run the following commands:

```bash
cd BlazorApp
dotnet run --urls=http://0.0.0.0:5000
```

## Access the application

After running the application:

- Open the **Ports** panel in Codespaces
- Locate port `5000`
- Click **Open in Browser**

The application will load in your browser.

## DataGrid implementation

This sample demonstrates the integration of the [Blazor DataGrid](https://www.syncfusion.com/blazor-components/blazor-datagrid) component within a Blazor Web App.

It shows how the DataGrid can be added and rendered using Interactive Server mode in a Codespaces-enabled environment.

## References

- [Getting Started with Blazor DataGrid in Blazor Web App](https://blazor.syncfusion.com/documentation/datagrid/getting-started-with-web-app)
- [Integrating Blazor DataGrid with PDF Viewer](https://blazor.syncfusion.com/documentation/common/integration/blazor-with-pdf-viewer)  