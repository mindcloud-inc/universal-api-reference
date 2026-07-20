# List Unsubscribed Subscribers with Campaign Monitor

Retrieves unsubscribed subscribers from a Campaign Monitor list.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/:listId/unsubscribed.json`
- **Base URL:** `https://api.createsend.com/api/v3.3`
- **Official documentation:** [List Unsubscribed Subscribers](https://www.campaignmonitor.com/api/v3-3/lists/#unsubscribed-subscribers-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `string` | yes | Campaign Monitor list identifier. |
