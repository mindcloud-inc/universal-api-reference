# Create URL Import Job with Canva

Creates a Canva URL import job.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/url-imports`
- **Base URL:** `https://api.canva.com/rest`
- **Official documentation:** [Create URL Import Job](https://www.canva.dev/docs/connect/api-reference/design-imports/create-url-import-job/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | A title for the design. |
| `url` | body | `string` | yes | The public URL of the file to import. |
| `mime_type` | body | `string` | no | Optional MIME type of the imported file. |
