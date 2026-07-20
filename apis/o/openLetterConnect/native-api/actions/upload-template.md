# Upload Template with Open Letter Connect

Uploads a template to Open Letter Connect.

## Endpoint

- **Method:** `POST`
- **Path:** `/templates/upload`
- **Base URL:** `https://api.openletterconnect.com/api/v1`
- **Official documentation:** [Upload Template](https://api-docs.openletterconnect.com/_templates/upload-template/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `backHtml` | body | `string` | no | The optional back-side HTML file to upload. |
| `html` | body | `string` | no | The front HTML file to upload. |
| `thumbnail` | body | `string` | no | The thumbnail file to upload. |
