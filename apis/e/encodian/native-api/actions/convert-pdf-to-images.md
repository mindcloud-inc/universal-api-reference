# Convert PDF To Images with Encodian

Converts a PDF document to images in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Conversion/ConvertPdfToImages`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Convert PDF To Images](https://support.encodian.com/hc/en-gb/articles/4418101623441)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FileContent` | body | `string` | yes | A Base64 encoded representation of the PDF file to be processed. |
| `ImageFormat` | body | `string` | yes | Set the format for the output image files. |
| `FilenamePrefix` | body | `string` | no | The prefix filename for the output image files. |
| `Resolution` | body | `number` | no | Set the output image resolution. |
