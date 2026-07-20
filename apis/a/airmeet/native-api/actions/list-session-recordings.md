# List Session Recordings with Airmeet

Finds session recording links in Airmeet.

## Endpoint

- **Method:** `GET`
- **Path:** `/airmeet/{airmeetId}/session-recordings`
- **Base URL:** `https://api-gateway-prod.us.airmeet.com/prod`
- **Official documentation:** [List Session Recordings](https://help.airmeet.com/support/solutions/articles/82000909768-1-event-details-airmeet-public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `airmeetId` | path | `string` | yes | The Airmeet event ID. |
| `sessionIds` | query | `string` | yes | Comma-separated session IDs to generate recording links for. |
