# List Category Topics with Discourse

Retrieves topics from a Discourse category.

## Endpoint

- **Method:** `GET`
- **Path:** `/c/:slug/:id.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [List Category Topics](https://docs.discourse.org/#tag/Categories/operation/listCategoryTopics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Numeric Discourse category ID. |
| `slug` | path | `string` | yes | Category slug used in the category URL. |
