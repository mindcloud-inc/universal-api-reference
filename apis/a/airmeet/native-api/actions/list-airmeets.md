# List Airmeets with Airmeet

Finds Airmeet events accessible to your token.

## Endpoint

- **Method:** `GET`
- **Path:** `/airmeets`
- **Base URL:** `https://api-gateway-prod.us.airmeet.com/prod`
- **Official documentation:** [List Airmeets](https://help.airmeet.com/support/solutions/articles/82000909768-1-event-details-airmeet-public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `string` | no | Fetch Airmeets created after this cursor. |
| `before` | query | `string` | no | Fetch Airmeets created before this cursor. |
| `size` | query | `number` | no | Number of Airmeets to return. Airmeet defaults to 50 and caps at 500. |
