# Get Site with Synchroteam

Retrieves a site from Synchroteam by supported identifier.

## Endpoint

- **Method:** `GET`
- **Path:** `/Api/v2/Site/Details`
- **Base URL:** `https://ws.synchroteam.com`
- **Official documentation:** [Get Site](https://api.synchroteam.com/v2/#get-site)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifierType` | query | `string` | yes | Which identifier to use (for example: name, id, myId). |
| `identifierValue` | query | `string` | yes | The identifier value. |
