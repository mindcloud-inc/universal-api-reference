# Create Parent Category with ClassMarker

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/categories/parent_category.json`
- **Base URL:** `https://api.classmarker.com`
- **Official documentation:** [Create Parent Category](https://www.classmarker.com/online-testing/docs/api/#post-parent-category)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parent_category_name` | body | `string` | yes | Name of the parent category to create. |
| `verify_only` | query | `boolean` | no | Validate the request without creating the parent category. |
