# Get Job Photos with Synchroteam

Retrieves photos for a job from Synchroteam.

## Endpoint

- **Method:** `GET`
- **Path:** `/Api/v2/Jobs/Photos`
- **Base URL:** `https://ws.synchroteam.com`
- **Official documentation:** [Get Job Photos](https://api.synchroteam.com/v2/#job-photos)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifierType` | query | `string` | yes | Which identifier to use (for example: num, id, myId). |
| `identifierValue` | query | `string` | yes | The identifier value. |
