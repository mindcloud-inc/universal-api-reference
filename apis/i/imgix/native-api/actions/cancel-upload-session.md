# Cancel Upload Session with imgix

Cancels an upload session in imgix.

## Endpoint

- **Method:** `DELETE`
- **Path:** `sources/:sourceId/upload-sessions/cancel/:sessionId`
- **Base URL:** `https://api.imgix.com/api/v1`
- **Official documentation:** [Cancel Upload Session](https://docs.imgix.com/en-US/apis/management/assets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | path | `string` | yes | The upload session id. |
| `sourceId` | path | `string` | yes | The imgix source_id. |
