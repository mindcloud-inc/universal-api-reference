# Create URL Asset Upload Job with Canva

Creates a URL asset upload job in Canva.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/url-asset-uploads`
- **Base URL:** `https://api.canva.com/rest`
- **Official documentation:** [Create URL Asset Upload Job](https://www.canva.dev/docs/connect/api-reference/assets/create-url-asset-upload-job/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | A name for the asset. Maximum length: 255. |
| `url` | body | `string` | yes | The publicly accessible internet URL of the file to import. Maximum length: 2048. |
