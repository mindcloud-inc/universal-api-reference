# Create Category with Turis

Creates a new category in Turis.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/public/v1/categories`
- **Base URL:** `https://{tenant}.turis.app`
- **Official documentation:** [Create Category](https://documenter.getpostman.com/view/16452985/TzkyP1Er)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category_custom_id` | body | `string` | no | Optional external category identifier. |
| `category_name` | body | `string` | no | Category name to create in Turis. |
| `parent_id` | body | `string` | no | Optional parent category ID. |
