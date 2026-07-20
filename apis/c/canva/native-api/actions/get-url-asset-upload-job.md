# Get URL Asset Upload Job with Canva

Retrieves a Canva URL asset upload job.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/url-asset-uploads/:jobId`
- **Base URL:** `https://api.canva.com/rest`
- **Official documentation:** [Get URL Asset Upload Job](https://www.canva.dev/docs/connect/api-reference/assets/get-url-asset-upload-job/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | The asset upload job ID. Maximum length: 50. |
