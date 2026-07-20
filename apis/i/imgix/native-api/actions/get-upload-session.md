# Get Upload Session with imgix

Retrieves an upload session from imgix.

## Endpoint

- **Method:** `GET`
- **Path:** `sources/:sourceId/upload-sessions/status/:sessionId`
- **Base URL:** `https://api.imgix.com/api/v1`
- **Official documentation:** [Get Upload Session](https://docs.imgix.com/en-US/apis/management/assets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | path | `string` | yes | The upload session id. |
| `sourceId` | path | `string` | yes | The imgix source_id. |
