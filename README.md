# Blazor File Upload Image Preview

## Overview

This sample demonstrates how to display an image preview before uploading files in a Blazor application using the Syncfusion [Blazor File Upload](https://www.syncfusion.com/blazor-components/blazor-file-upload) component.

The application allows users to select image files and review them before they are uploaded. Previewing images prior to upload helps users validate file selection, reduce mistakes, and improve the overall upload experience.

Implementation-specific details such as exact page names, APIs, and event handlers could not be verified from the publicly accessible source files during review and are therefore identified with verification notes where appropriate.

## Key Features

- **Upload Large Files** - Efficiently upload large files using chunk-based uploading, where files are divided into smaller segments and transferred sequentially to improve reliability and performance.

- **Resumable Upload** - Pause, resume, retry, or cancel uploads with built-in resumable functionality, ensuring reliable transfer of large files and media assets.

- **Multiple File Upload** - Select and upload multiple files simultaneously, making it ideal for gallery management, document sharing, and bulk uploads.

- **Drag-and-Drop Support** - Simplify file selection by dragging files directly into the upload area for a more intuitive user experience.

- **Customizable Upload UI** - Customize action buttons, file lists, and overall upload interface to match application requirements and branding.

- **File Type Restrictions** - Restrict uploads to specific file extensions or formats to ensure only valid files are accepted.

- **File Validation** - Validate file size, file count, total upload size, and MIME types before uploading files to the server.

- **Folder Upload** - Upload entire folders, including nested subfolders and files, in a single operation.

- **Paste Image Upload** - Upload images directly from the clipboard by copying and pasting them into the uploader.

- **Delete Uploaded Files** - Remove previously uploaded files from the server through a built-in file management interface.

- **Preloaded Files** - Display and manage files that were uploaded previously by loading them into the uploader with a completed state.

- **Auto Upload** - Automatically start file uploads immediately after files are selected and added to the upload queue.

- **Progress Tracking** - Display customizable progress indicators and upload percentages to provide real-time upload status.

- **Localization Support** - Translate built-in uploader text and messages using localization resources to support multiple languages.

- **Right-to-Left (RTL) Support** - Enable RTL rendering for languages that require right-to-left text direction.

- **HTML Form Integration** - Integrate the uploader with standard HTML forms for synchronous form submission scenarios.

## Prerequisites

- [Visual Studio 2022](https://visualstudio.microsoft.com/vs/) or [Visual Studio Code](https://code.visualstudio.com/)
- [.NET SDK](https://dotnet.microsoft.com/en-us/download/dotnet) compatible with the project's target framework

## How to Run the Project

**Visual Studio 2022**

1. Clone or download the repository.
2. Open the solution file:

   `UploadImagePreview.sln`

3. Restore NuGet packages.
4. Build the solution.
5. If necessary, set the appropriate startup project.
6. Run the application using `Ctrl+F5`.

**Visual Studio Code**

1. Clone or download this repository.
2. Open the repository folder in Visual Studio Code.
3. Open the integrated terminal.
4. Navigate to the project directory.

```bash
dotnet restore
dotnet run
```

5. Open the application in the browser.

## Project Structure

- `Client/Model/UserDetails.cs` - Data model used by the entry form. Defines user information fields (`FirstName`, `LastName`, and `Email`) with Data Annotations validation.

- `Client/Pages/Index.razor` - Main sample page demonstrating image preview before upload using the Syncfusion Blazor File Upload component (`SfUploader`). Implements:
  - Form validation using `EditForm` and `DataAnnotationsValidator`
  - User information collection
  - Image file selection with file type restrictions (`.png`, `.jpg`, `.jpeg`)
  - Real-time image preview generation using Base64 image data
  - Custom uploader templates
  - File upload and removal event handling (`ValueChange`, `OnRemove`)
  - Upload submission to the server through an HTTP API endpoint

- `Client/Pages/FetchData.razor` - Default Blazor sample page that retrieves and displays weather forecast data from the server using `HttpClient`.

- `Server/Controllers/WeatherForecastController.cs` - ASP.NET Core Web API controller that provides sample weather forecast data consumed by the `FetchData.razor` page.

- `Shared/WeatherForecast.cs` - Shared model used by both the Client and Server projects for weather forecast data exchange.

## Support and Feedback

- For general product questions, visit the [Syncfusion Community Forum](https://www.syncfusion.com/forums) or [Syncfusion Support](https://www.syncfusion.com/support).
- To report an issue specific to this sample, open a GitHub issue in this repository.
- File Upload documentation : https://blazor.syncfusion.com/documentation/file-upload/getting-started

## License

This is a Syncfusion sample project provided to demonstrate product usage. Review the [Syncfusion license terms](https://www.syncfusion.com/sales/pricing?category=ui-components) before using Syncfusion components in your own applications.