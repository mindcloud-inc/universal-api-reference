# List Booth Attendees with Airmeet

Finds booth attendance records in Airmeet.

## Endpoint

- **Method:** `GET`
- **Path:** `/airmeet/{airmeetId}/booth/{boothId}/booth-attendance`
- **Base URL:** `https://api-gateway-prod.us.airmeet.com/prod`
- **Official documentation:** [List Booth Attendees](https://help.airmeet.com/support/solutions/articles/82000909768-1-event-details-airmeet-public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `string` | no | Fetch booth attendance after this cursor. |
| `airmeetId` | path | `string` | yes | The Airmeet event ID. |
| `before` | query | `string` | no | Fetch booth attendance before this cursor. |
| `boothId` | path | `string` | yes | The booth ID. |
| `size` | query | `number` | no | Number of booth attendance records to return per page, between 1 and 50. |
