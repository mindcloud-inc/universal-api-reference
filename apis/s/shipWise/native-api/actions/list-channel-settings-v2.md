# List Channel Settings V2 with ShipWise

Retrieves channel settings from ShipWise.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/Channel/settings`
- **Base URL:** `https://api.shipwise.com/`
- **Official documentation:** [List Channel Settings V2](https://api.shipwise.com/swagger/v2/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `linkIds` | query | `string` | yes | One or more ShipWise channel link IDs to retrieve settings for. |
