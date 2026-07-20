# List Subscriber History with Campaign Monitor

Retrieves history for a Campaign Monitor subscriber by email address.

## Endpoint

- **Method:** `GET`
- **Path:** `/subscribers/:listId/history.json`
- **Base URL:** `https://api.createsend.com/api/v3.3`
- **Official documentation:** [List Subscriber History](https://www.campaignmonitor.com/api/v3-3/subscribers/#getting-subscribers-history)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `string` | yes | Campaign Monitor list identifier. |
| `email` | query | `string` | yes | Subscriber email address. |
