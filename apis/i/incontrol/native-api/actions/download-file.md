# Download File with Incontrol

Downloads a file from Incontrol.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/file/{{id}}/download`
- **Base URL:** `https://portal.incontrol.app`
- **Official documentation:** [Download File](https://portal.incontrol.app/swagger/index.html?urls.primaryName=Public%20API%20(v1))

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The file ID. |
| `sourceType` | query | `string` | yes | The origin type of the file (for security purpose). |
| `sourceId` | query | `string` | yes | The ID of the origin type of the file (for security purpose). |
