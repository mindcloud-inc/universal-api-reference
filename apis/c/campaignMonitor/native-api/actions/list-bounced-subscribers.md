# List Bounced Subscribers with Campaign Monitor

Retrieves bounced subscribers from a Campaign Monitor list.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/:listId/bounced.json`
- **Base URL:** `https://api.createsend.com/api/v3.3`
- **Official documentation:** [List Bounced Subscribers](https://www.campaignmonitor.com/api/v3-3/lists/#bounced-subscribers-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `string` | yes | Campaign Monitor list identifier. |
