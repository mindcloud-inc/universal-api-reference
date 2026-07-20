# Get Subscriber Details with Campaign Monitor

Retrieves a Campaign Monitor subscriber by email address.

## Endpoint

- **Method:** `GET`
- **Path:** `/subscribers/:listId.json`
- **Base URL:** `https://api.createsend.com/api/v3.3`
- **Official documentation:** [Get Subscriber Details](https://www.campaignmonitor.com/api/v3-3/subscribers/#getting-a-subscribers-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `string` | yes | Campaign Monitor list identifier. |
| `email` | query | `string` | yes | Subscriber email address. |
| `includetrackingpreference` | query | `boolean` | no | Include subscriber consent-to-track values. Default is false. |
