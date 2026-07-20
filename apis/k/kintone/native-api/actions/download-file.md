# Download File with Kintone

Downloads a file from Kintone.

## Endpoint

- **Method:** `GET`
- **Path:** `/file.json`
- **Base URL:** `{baseUrl}/k/v1`
- **Official documentation:** [Download File](https://kintone.dev/en/docs/kintone/rest-api/files/download-file/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileKey` | query | `string` | yes | The Kintone file key returned by an upload or file field. |
