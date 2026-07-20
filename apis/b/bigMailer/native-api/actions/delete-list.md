# Delete List with BigMailer

Deletes a list from BigMailer while keeping contacts intact.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/brands/:brand_id/lists/:list_id`
- **Base URL:** `https://api.bigmailer.io/v1`
- **Official documentation:** [Delete List](https://docs.bigmailer.io/reference/deletelist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `brand_id` | path | `string` | yes | ID of the brand containing the list. |
| `list_id` | path | `string` | yes | ID of the list. |
