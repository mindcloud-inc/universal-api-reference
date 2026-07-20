# List Contacts with Seven

Retrieves contacts from Seven.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://gateway.seven.io/api`
- **Official documentation:** [List Contacts](https://docs.seven.io/en/rest-api/endpoints/contacts#query-contact-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_by` | query | `string` | no | The column by which the contacts should be sorted. |
| `order_direction` | query | `string` | no | The direction of the sorting. Can be either asc or desc . |
| `search` | query | `string` | no | You can use this parameter to search in all columns in your contacts. |
| `offset` | query | `number` | no | The page to be displayed. |
| `limit` | query | `number` | no | The number of contacts to be displayed per page. Can be a value between 30 and 500 . |
| `group_id` | query | `number` | no | Only display contacts who are members of a specific group. |
