# Create Category with Discourse

Creates a new category in Discourse.

## Endpoint

- **Method:** `POST`
- **Path:** `/categories.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Create Category](https://docs.discourse.org/#tag/Categories/operation/createCategory)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Category name. |
| `color` | body | `string` | no | Category color hex code without #. |
