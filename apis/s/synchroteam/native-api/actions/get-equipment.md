# Get Equipment with Synchroteam

Retrieves equipment from Synchroteam by supported identifier.

## Endpoint

- **Method:** `GET`
- **Path:** `/Api/v2/Equipment/Details`
- **Base URL:** `https://ws.synchroteam.com`
- **Official documentation:** [Get Equipment](https://api.synchroteam.com/v2/#get-equipment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifierType` | query | `string` | yes | Which identifier to use (for example: name, id, myId). |
| `identifierValue` | query | `string` | yes | The identifier value. |
