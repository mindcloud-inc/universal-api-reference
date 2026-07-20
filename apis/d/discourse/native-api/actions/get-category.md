# Get Category with Discourse

Retrieves a forum category from Discourse.

## Endpoint

- **Method:** `GET`
- **Path:** `/c/:id/show.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Get Category](https://docs.discourse.org/#tag/Categories/operation/getCategory)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Numeric Discourse category ID. |
