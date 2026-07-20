# Delete Subscriber with CreateSend

Deletes an existing subscriber from CreateSend by email address.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/subscribers/:listId.json`
- **Base URL:** `https://api.createsend.com/api/v3.3`
- **Official documentation:** [Delete Subscriber](https://www.campaignmonitor.com/api/v3-3/subscribers/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `listId` | path | `string` | yes |
| `email` | query | `string` | yes |
