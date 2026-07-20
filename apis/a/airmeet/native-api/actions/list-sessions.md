# List Sessions with Airmeet

Finds sessions in a specific Airmeet event.

## Endpoint

- **Method:** `GET`
- **Path:** `/airmeet/{airmeetId}/info`
- **Base URL:** `https://api-gateway-prod.us.airmeet.com/prod`
- **Official documentation:** [List Sessions](https://help.airmeet.com/support/solutions/articles/82000909768-1-event-details-airmeet-public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `airmeetId` | path | `string` | yes | The Airmeet event ID. |
