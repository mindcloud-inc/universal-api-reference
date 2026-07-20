# Create Category with Edoobox

Creates a new category in Edoobox.

## Endpoint

- **Method:** `POST`
- **Path:** `/category`
- **Base URL:** `https://app2.edoobox.com/v2`
- **Official documentation:** [Create Category](https://api.docs.edoobox.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Category name. |
| `design` | body | `string` | yes | edoobox design ID for the category. |
| `category` | body | `string` | no | Parent edoobox category ID. |
| `type` | body | `string` | yes | edoobox category type. |
