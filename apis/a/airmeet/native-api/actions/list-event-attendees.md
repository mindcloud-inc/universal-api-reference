# List Event Attendees with Airmeet

Finds event attendance records in Airmeet.

## Endpoint

- **Method:** `GET`
- **Path:** `/airmeet/{airmeetId}/attendees`
- **Base URL:** `https://api-gateway-prod.us.airmeet.com/prod`
- **Official documentation:** [List Event Attendees](https://help.airmeet.com/support/solutions/articles/82000909768-1-event-details-airmeet-public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `string` | no | Fetch attendees after this cursor. |
| `airmeetId` | path | `string` | yes | The Airmeet event ID. |
| `before` | query | `string` | no | Fetch attendees before this cursor. |
| `size` | query | `number` | no | Number of attendees to return per page, between 1 and 50. |
