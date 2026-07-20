# List Unconfirmed Subscribers with Campaign Monitor

Retrieves unconfirmed subscribers from a Campaign Monitor list.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/:listId/unconfirmed.json`
- **Base URL:** `https://api.createsend.com/api/v3.3`
- **Official documentation:** [List Unconfirmed Subscribers](https://www.campaignmonitor.com/api/v3-3/lists/#unconfirmed-subscribers-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `string` | yes | Campaign Monitor list identifier. |
