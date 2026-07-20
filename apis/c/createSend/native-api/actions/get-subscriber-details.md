# Get Subscriber Details with CreateSend

Retrieves subscriber details from CreateSend by email address.

## Endpoint

- **Method:** `GET`
- **Path:** `/subscribers/:listId.json`
- **Base URL:** `https://api.createsend.com/api/v3.3`
- **Official documentation:** [Get Subscriber Details](https://www.campaignmonitor.com/api/v3-3/subscribers/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `listId` | path | `string` | yes |
| `email` | query | `string` | yes |
| `includetrackingpreference` | query | `boolean` | no |
