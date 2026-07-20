# Get Job Detail with Synchroteam

Retrieves a job from Synchroteam by supported identifier.

## Endpoint

- **Method:** `GET`
- **Path:** `/Api/v2/Jobs/Detail`
- **Base URL:** `https://ws.synchroteam.com`
- **Official documentation:** [Get Job Detail](https://api.synchroteam.com/v2/#get-job-detail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifierType` | query | `string` | yes | Which identifier to use (for example: num, id, myId). |
| `identifierValue` | query | `string` | yes | The identifier value. |
