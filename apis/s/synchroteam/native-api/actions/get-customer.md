# Get Customer with Synchroteam

Retrieves a customer from Synchroteam by supported identifier.

## Endpoint

- **Method:** `GET`
- **Path:** `/Api/v2/Customer/Details`
- **Base URL:** `https://ws.synchroteam.com`
- **Official documentation:** [Get Customer](https://api.synchroteam.com/v2/#get-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifierType` | query | `string` | yes | Which identifier to use (for example: name, id, myId, email). |
| `identifierValue` | query | `string` | yes | The identifier value. |
