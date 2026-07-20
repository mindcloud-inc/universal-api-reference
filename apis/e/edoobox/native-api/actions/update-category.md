# Update Category with Edoobox

Updates an existing category in Edoobox.

## Endpoint

- **Method:** `PUT`
- **Path:** `/category/:category_id`
- **Base URL:** `https://app2.edoobox.com/v2`
- **Official documentation:** [Update Category](https://api.docs.edoobox.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category_id` | path | `string` | yes | edoobox category ID. |
| `design` | body | `string` | no | edoobox design ID to set on the category. |
| `prevent_multiple_bookings` | body | `string` | no | Duplicate-booking prevention mode. |
| `internal_code` | body | `string` | no | Internal code for the category. |
