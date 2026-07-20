# Validate Job with Synchroteam

Validates a job in Synchroteam by supported identifier.

## Endpoint

- **Method:** `PUT`
- **Path:** `/Api/v2/Jobs/Validate`
- **Base URL:** `https://ws.synchroteam.com`
- **Official documentation:** [Validate Job](https://api.synchroteam.com/v2/#validate-job)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifierType` | query | `string` | yes | Which identifier to use (for example: num, id, myId). |
| `identifierValue` | query | `string` | yes | The identifier value. |
