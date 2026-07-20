# Open Upload Session with imgix

Opens an upload session in imgix.

## Endpoint

- **Method:** `POST`
- **Path:** `sources/:sourceId/upload-sessions/create/:originPath`
- **Base URL:** `https://api.imgix.com/api/v1`
- **Official documentation:** [Open Upload Session](https://docs.imgix.com/en-US/apis/management/assets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `originPath` | path | `string` | yes | The destination origin path for the large upload session. |
| `sourceId` | path | `string` | yes | The imgix source_id. |
