# Close Upload Session with imgix

## Endpoint

- **Method:** `POST`
- **Path:** `sources/:sourceId/upload-sessions/:sessionId`
- **Base URL:** `https://api.imgix.com/api/v1`
- **Official documentation:** [Close Upload Session](https://docs.imgix.com/en-US/apis/management/assets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | path | `string` | yes | The upload session id. |
| `sourceId` | path | `string` | yes | The imgix source_id. |
