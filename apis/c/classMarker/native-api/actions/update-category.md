# Update Category with ClassMarker

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/category/{category_id}.json`
- **Base URL:** `https://api.classmarker.com`
- **Official documentation:** [Update Category](https://www.classmarker.com/online-testing/docs/api/#put-category)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category_id` | path | `number` | yes | Numeric ClassMarker category ID. |
| `category_name` | body | `string` | yes | Updated name for the category. |
| `parent_category_id` | body | `number` | yes | Numeric ClassMarker parent category ID that will own the category. |
| `verify_only` | query | `boolean` | no | Validate the request without updating the category. |
