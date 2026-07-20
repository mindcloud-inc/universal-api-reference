# List Leads with Instantly

Retrieves leads from Instantly.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/leads/list`
- **Base URL:** `https://api.instantly.ai`
- **Official documentation:** [List Leads](https://developer.instantly.ai/api-reference/lead/list-leads)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | body | `string` | no | List ID to filter leads. |
| `limit` | body | `number` | no | Number of leads to return. |
