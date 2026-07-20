# Delete Subscriber with Campaign Monitor

Deletes a subscriber from a Campaign Monitor list by email address.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/subscribers/:listId.json`
- **Base URL:** `https://api.createsend.com/api/v3.3`
- **Official documentation:** [Delete Subscriber](https://www.campaignmonitor.com/api/v3-3/subscribers/#deleting-a-subscriber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `string` | yes | Campaign Monitor list identifier. |
| `email` | query | `string` | yes | Subscriber email address to delete. |
