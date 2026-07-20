# Cancel Job with Synchroteam

Cancels a job in Synchroteam by supported identifier.

## Endpoint

- **Method:** `PUT`
- **Path:** `/Api/v2/Jobs/Cancel`
- **Base URL:** `https://ws.synchroteam.com`
- **Official documentation:** [Cancel Job](https://api.synchroteam.com/v2/#cancel-job)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifierType` | query | `string` | yes | Which identifier to use (for example: num, id, myId). |
| `identifierValue` | query | `string` | yes | The identifier value. |
