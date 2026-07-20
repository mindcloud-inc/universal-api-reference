# Create Email List Record with Toofr

Creates a new email list record in Toofr.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists/:list_id/list_records`
- **Base URL:** `https://www.findemails.com/api/v1`
- **Official documentation:** [Create Email List Record](https://developer.findemails.com/?from=explinks.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | query | `string` | yes | Record company name. |
| `first_name` | query | `string` | yes | Record first name. |
| `last_name` | query | `string` | yes | Record last name. |
| `list_id` | path | `string` | yes | Email list ID. |
