# Convert - HTML to Image with Encodian - Convert

Creates an image file from HTML or a web URL in Encodian - Convert.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Conversion/HtmlToImage`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Convert - HTML to Image](https://support.encodian.com/hc/en-gb/articles/13961998920732)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `htmlData` | body | `string` | no | Raw HTML content to convert. |
| `fileContent` | body | `file` | no | HTML file content to convert. |
| `Url` | body | `string` | no | Web page URL to convert. |
| `imgWidth` | body | `number` | no | Output image width in pixels. |
| `imgHeight` | body | `number` | no | Output image height in pixels. |
