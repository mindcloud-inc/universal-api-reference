# List Questions Asked with Airmeet

Finds questions asked in a specific Airmeet.

## Endpoint

- **Method:** `GET`
- **Path:** `/airmeet/{airmeetId}/questions`
- **Base URL:** `https://api-gateway-prod.us.airmeet.com/prod`
- **Official documentation:** [List Questions Asked](https://help.airmeet.com/support/solutions/articles/82000909768-1-event-details-airmeet-public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `airmeetId` | path | `string` | yes | The Airmeet event ID. |
