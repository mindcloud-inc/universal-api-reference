# List Tags with Timely

Retrieves tags from Timely.

## Endpoint

- **Method:** `GET`
- **Path:** `/1.1/{account_id}/labels`
- **Base URL:** `https://api.timelyapp.com`
- **Official documentation:** [List Tags](https://developer.timely.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | Account ID |
| `limit` | query | `number` | no | Maximum number of labels to return (default: 10000) |
| `offset` | query | `number` | no | Number of labels to skip (default: 0) |
| `filter` | query | `string` | no | Filter labels by status: all (default), active, or archived |
| `parent_id` | query | `number` | no | Filter by parent label ID to get child labels only |
