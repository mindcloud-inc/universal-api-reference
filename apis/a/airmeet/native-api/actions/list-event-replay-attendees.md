# List Event Replay Attendees with Airmeet

Finds event replay attendees in Airmeet.

## Endpoint

- **Method:** `GET`
- **Path:** `/airmeet/{airmeetId}/event-replay-attendees`
- **Base URL:** `https://api-gateway-prod.us.airmeet.com/prod`
- **Official documentation:** [List Event Replay Attendees](https://help.airmeet.com/support/solutions/articles/82000909768-1-event-details-airmeet-public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `string` | no | Fetch replay attendance after this cursor. |
| `airmeetId` | path | `string` | yes | The Airmeet event ID. |
| `before` | query | `string` | no | Fetch replay attendance before this cursor. |
| `size` | query | `number` | no | Number of replay attendance records to return per page, between 1 and 50. |
