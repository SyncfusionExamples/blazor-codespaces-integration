# Blazor Codespaces Integration

## Overview

This sample demonstrates how to run a Blazor Web App with Interactive Server rendering in [GitHub Codespaces](https://docs.github.com/en/codespaces/about-codespaces) while integrating the Syncfusion [Blazor DataGrid](https://www.syncfusion.com/blazor-components/blazor-datagrid). The repository includes a preconfigured development container that automatically prepares the required .NET environment, restores dependencies, and forwards application ports for browser access.

The sample is designed for developers who want to evaluate, learn, or develop Syncfusion Blazor applications without setting up a complete local development environment. By using GitHub Codespaces, the application can be built, run, and tested entirely from the browser with minimal configuration.

## Key Features

- Interactive Server rendering enabled through the `@rendermode InteractiveServer` directive.
- Data binding implemented through the `DataSource` property of the `SfGrid` component.
- Runtime generation of sample order records in the `OnInitialized()` lifecycle method.
- Strongly typed `Order` model containing `OrderID`, `CustomerName`, `ShipCity`, `OrderDate`, and `Freight` properties.
- Automatic display of model fields as DataGrid columns through Syncfusion's auto-generated column feature.
- Sample data generation using randomized customer names and shipping cities for DataGrid population.
- GitHub Codespaces development environment configured using a prebuilt .NET 10 development container.
- Automatic installation of WebAssembly tools through the `postCreateCommand` container initialization step.
- Automatic NuGet package restoration through the `postStartCommand` configuration.
- Port forwarding configured for port 5000 with automatic browser launch when the application starts.
- Preconfigured Visual Studio Code extensions for C#, Blazor, Docker, GitHub Codespaces, and .NET development.
- Development environment variables configured for ASP.NET Core Development mode and container-based execution.

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

## Project Structure

`.devcontainer/devcontainer.json` - GitHub Codespaces development container configuration, .NET 10 SDK image selection, VS Code extension setup, port forwarding, environment variables, and automated initialization commands.

`Pages/Home.razor` - Main application page routed to `/` that demonstrates the Syncfusion DataGrid using Interactive Server rendering and displays generated order data through the `SfGrid` component.

## Support and Feedback

- For general product questions, visit the [Syncfusion Community Forum](https://www.syncfusion.com/forums) or [Syncfusion Support](https://www.syncfusion.com/support).
- To report an issue specific to this sample, open a GitHub issue in this repository.
- Official documentation: https://blazor.syncfusion.com/documentation/common/integration/blazor-with-github-codespaces
- [Getting Started with Blazor DataGrid in Blazor Web App](https://blazor.syncfusion.com/documentation/datagrid/getting-started-with-web-app)

## License

This is a Syncfusion sample project provided to demonstrate product usage. Review the [Syncfusion license terms](https://www.syncfusion.com/sales/pricing?category=ui-components) before using Syncfusion components in your own applications.