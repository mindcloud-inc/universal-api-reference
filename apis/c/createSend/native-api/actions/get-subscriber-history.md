# Get Subscriber History with CreateSend

Retrieves subscriber history from CreateSend by email address.

## Endpoint

- **Method:** `GET`
- **Path:** `/subscribers/:listId/history.json`
- **Base URL:** `https://api.createsend.com/api/v3.3`
- **Official documentation:** [Get Subscriber History](https://www.campaignmonitor.com/api/v3-3/subscribers/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `listId` | path | `string` | yes |
| `email` | query | `string` | yes |
