# List Active Subscribers with Campaign Monitor

Retrieves active subscribers from a Campaign Monitor list.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/:listId/active.json`
- **Base URL:** `https://api.createsend.com/api/v3.3`
- **Official documentation:** [List Active Subscribers](https://www.campaignmonitor.com/api/v3-3/lists/#active-subscribers-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `string` | yes | Campaign Monitor list identifier. |
| `date` | query | `string` | no | Return subscribers who became active on or after this date in YYYY-MM-DD format. |
| `page` | query | `number` | no | Results page to retrieve. Default is 1. |
| `pagesize` | query | `number` | no | Number of records to retrieve per results page. Default is 1000. |
| `orderfield` | query | `string` | no | Field used to order results: email, name, or date. |
| `orderdirection` | query | `string` | no | Direction used to order results: asc or desc. |
| `includetrackingpreference` | query | `boolean` | no | Include subscriber consent-to-track values. Default is false. |
