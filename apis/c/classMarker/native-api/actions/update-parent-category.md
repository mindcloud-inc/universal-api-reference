# Update Parent Category with ClassMarker

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/categories/parent_category/{parent_category_id}.json`
- **Base URL:** `https://api.classmarker.com`
- **Official documentation:** [Update Parent Category](https://www.classmarker.com/online-testing/docs/api/#put-parent-category)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parent_category_id` | path | `number` | yes | Numeric ClassMarker parent category ID. |
| `parent_category_name` | body | `string` | yes | Updated name for the parent category. |
| `verify_only` | query | `boolean` | no | Validate the request without updating the parent category. |
