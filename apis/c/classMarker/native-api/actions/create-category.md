# Create Category with ClassMarker

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/categories/category.json`
- **Base URL:** `https://api.classmarker.com`
- **Official documentation:** [Create Category](https://www.classmarker.com/online-testing/docs/api/#post-category)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category_name` | body | `string` | yes | Name of the category to create. |
| `parent_category_id` | body | `number` | yes | Numeric ClassMarker parent category ID that will own the category. |
| `verify_only` | query | `boolean` | no | Validate the request without creating the category. |
