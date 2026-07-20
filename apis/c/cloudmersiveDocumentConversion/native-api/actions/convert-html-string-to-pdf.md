# Convert HTML String to PDF with Cloudmersive Document Conversion

Converts an HTML string to PDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/convert/web/html/to/pdf`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Convert HTML String to PDF](https://api.cloudmersive.com/docs/convert.asp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Html` | body | `string` | yes | HTML string to render into a PDF. |
| `ExtraLoadingWait` | body | `number` | no | Optional extra wait time in milliseconds for dynamic content. Maximum is 30000. |
| `IncludeBackgroundGraphics` | body | `boolean` | no | Optional. Set true to include background graphics in the PDF; default is true. |
| `ScaleFactor` | body | `number` | no | Optional scale factor percentage. Default is 100. |
| `AutoSanitize` | body | `boolean` | no | Optional. Automatically sanitize unsafe HTML elements. Default is true. |
