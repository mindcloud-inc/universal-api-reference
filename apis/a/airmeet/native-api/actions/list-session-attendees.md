# List Session Attendees with Airmeet

Finds session attendance records in Airmeet.

## Endpoint

- **Method:** `GET`
- **Path:** `/session/{sessionId}/attendees`
- **Base URL:** `https://api-gateway-prod.us.airmeet.com/prod`
- **Official documentation:** [List Session Attendees](https://help.airmeet.com/support/solutions/articles/82000909768-1-event-details-airmeet-public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `string` | no | Fetch attendees after this cursor. |
| `before` | query | `string` | no | Fetch attendees before this cursor. |
| `sessionId` | path | `string` | yes | The Airmeet session ID. |
| `size` | query | `number` | no | Number of attendees to return per page, between 1 and 50. |
