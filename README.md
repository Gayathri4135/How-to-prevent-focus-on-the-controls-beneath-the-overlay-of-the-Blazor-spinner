# How to Prevent Focus on Controls Beneath the Overlay of the Blazor Spinner

## Overview

This sample demonstrates how to restrict user interaction with page elements while a loading overlay is active by using the Syncfusion [Blazor Spinner](https://www.syncfusion.com/forums). Preventing keyboard focus from moving to controls beneath an active overlay helps maintain a consistent user experience and improves accessibility when background content should not be interacted with during processing.

The sample shows a Blazor application that displays a spinner overlay and blocks focus from reaching controls that are visually covered by the loading layer.

## Key Features

- Uses the `SfSpinner` component to display a loading overlay.
- Controls spinner visibility through the `@bind-Visible` property.
- Sets `Label="Loading"` to provide loading status text.
- Applies `CssClass="e-spin-overlay"` to render the spinner as an overlay.
- Uses `ZIndex="1000"` to ensure the overlay remains above page controls.
- References the spinner instance through `@ref`.
- Triggers overlay activation using the `SfButton` `@onclick` event.
- Demonstrates interaction blocking with a `SfTextBox` control beneath the overlay.
- Invokes the JavaScript function `accessDOMElement` through `IJSRuntime.InvokeAsync()`.
- Uses `aria-modal="true"`, `role="dialog"`, and `tabindex="-1"` to support focus management and accessibility.

## Prerequisites

- [Visual Studio 2022](https://visualstudio.microsoft.com/vs/) or [Visual Studio Code](https://code.visualstudio.com/)
- [.NET SDK](https://dotnet.microsoft.com/en-us/download/dotnet) compatible with the project's target framework

## How to Run the Project

**Visual Studio 2022**

1. Clone or download this repository.
2. Open the `SpinnerOverlay.sln` solution file.
3. Restore NuGet packages.
4. Build the solution.
5. Run the application using **Ctrl+F5**.

**Visual Studio Code**

1. Clone the repository.
2. Open the repository folder in Visual Studio Code.
3. Open the integrated terminal.
4. Navigate to the startup project directory for the hosted application.

```bash
dotnet restore
dotnet run
```

5. Open the local URL displayed in the terminal after the application starts.

## Project Structure

- `SpinnerOverlay.sln` — Visual Studio solution file containing the sample projects.

- `Pages/Index.razor` — Main sample page that demonstrates preventing focus on controls beneath a Syncfusion Spinner overlay. Contains SfSpinner, SfButton, SfTextBox, and JavaScript interop logic.

## Support and Feedback

- For general product questions, visit the [Syncfusion Community Forum](https://www.syncfusion.com/forums) or [Syncfusion Support](https://www.syncfusion.com/support).
- To report an issue specific to this sample, open a GitHub issue in this repository.
- For implementation details, see the [relevant official Syncfusion documentation](https://blazor.syncfusion.com/documentation/progress-bar/getting-started).

## License

This is a Syncfusion sample project provided to demonstrate product usage. Review the [Syncfusion license terms](https://www.syncfusion.com/sales/pricing?category=ui-components) before using Syncfusion components in your own applications.