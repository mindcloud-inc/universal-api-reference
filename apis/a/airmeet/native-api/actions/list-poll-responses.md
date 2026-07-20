# List Poll Responses with Airmeet

Finds poll responses in a specific Airmeet.

## Endpoint

- **Method:** `GET`
- **Path:** `/airmeet/{airmeetId}/polls`
- **Base URL:** `https://api-gateway-prod.us.airmeet.com/prod`
- **Official documentation:** [List Poll Responses](https://help.airmeet.com/support/solutions/articles/82000909768-1-event-details-airmeet-public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `string` | no | Fetch poll responses after this cursor. |
| `airmeetId` | path | `string` | yes | The Airmeet event ID. |
| `before` | query | `string` | no | Fetch poll responses before this cursor. |
| `size` | query | `number` | no | Number of poll responses to return per page, between 1 and 50. |
