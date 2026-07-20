# List Booths with Airmeet

Finds booths in a specific Airmeet event.

## Endpoint

- **Method:** `GET`
- **Path:** `/airmeet/{airmeetId}/booths`
- **Base URL:** `https://api-gateway-prod.us.airmeet.com/prod`
- **Official documentation:** [List Booths](https://help.airmeet.com/support/solutions/articles/82000909768-1-event-details-airmeet-public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `airmeetId` | path | `string` | yes | The Airmeet event ID. |
