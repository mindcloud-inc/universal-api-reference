# Update Lead List with Instantly

Updates an existing lead list in Instantly.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/lead-lists/:id`
- **Base URL:** `https://api.instantly.ai`
- **Official documentation:** [Update Lead List](https://developer.instantly.ai/api/v2/leadlist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Lead list ID. |
| `name` | body | `string` | yes | Updated lead list name. |
