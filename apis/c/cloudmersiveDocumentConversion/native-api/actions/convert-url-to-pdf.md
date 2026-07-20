# Convert URL to PDF with Cloudmersive Document Conversion

Converts a website URL to PDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/convert/web/url/to/pdf`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Convert URL to PDF](https://api.cloudmersive.com/docs/convert.asp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Url` | body | `string` | yes | Website URL to render into a PDF. |
| `ExtraLoadingWait` | body | `number` | no | Optional extra wait time in milliseconds for page rendering. Maximum is 20000. |
| `IncludeBackgroundGraphics` | body | `boolean` | no | Optional. Set true to include background graphics in the PDF; default is true. |
| `ScaleFactor` | body | `number` | no | Optional scale factor percentage. Default is 100. |
