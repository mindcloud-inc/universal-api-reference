# Grade Items with Loop Returns

Grade the condition of return line items.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.loopreturns.com/api/v1/dispositioning/grade`
- **Base URL:** `https://api.loopreturns.com/api/v1`
- **Official documentation:** [Grade Items](https://docs.loopreturns.com/api-reference/latest/item-grading-and-disposition/grade-items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `items[]` | body | `array<object>` | no | An array of items to grade.  Max 30 items per request. |
| `items[].line_item_id` | body | `number` | yes | (required) The unique identifier associated with the line item. |
| `items[].description` | body | `string` | yes | The description of the item's condition. Max 255 characters. Maximum length: 255. |
| `items[].condition_category` | body | `list<string>` | no | The condition of the returned item.  Available options: `grade_a`, `grade_b`, `grade_c`, `grade_d`, `incorrect_item`, `missing, junk` |
| `items[].return_processor` | body | `string` | no | The email address of the warehouse partner used to process returns. Max 100 characters. Maximum length: 100. |
| `items[].note` | body | `string` | no | Any additional notes on the item's condition. Maximum length: 65535. |
| `items[].images[]` | body | `array<string>` | no | Add up to 5 images to show the items condition.  Max 5 URLs Max 2048 characters. Maximum length: 2048. |
| `items[].inspected_at` | body | `string` | no | The date and time at which the item was inspected, using the ISO 8601 date format. |
