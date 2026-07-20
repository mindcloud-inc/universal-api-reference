# Get Part Detail with Synchroteam

Retrieves a part from Synchroteam by supported identifier.

## Endpoint

- **Method:** `GET`
- **Path:** `/Api/v2/Part/Details`
- **Base URL:** `https://ws.synchroteam.com`
- **Official documentation:** [Get Part Detail](https://api.synchroteam.com/v2/#get-part-detail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifierType` | query | `string` | yes | Which identifier to use (for example: reference, id). |
| `identifierValue` | query | `string` | yes | The identifier value. |
