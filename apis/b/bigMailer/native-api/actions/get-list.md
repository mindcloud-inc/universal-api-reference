# Get List with BigMailer

Retrieves a list from a BigMailer brand.

## Endpoint

- **Method:** `GET`
- **Path:** `/brands/:brand_id/lists/:list_id`
- **Base URL:** `https://api.bigmailer.io/v1`
- **Official documentation:** [Get List](https://docs.bigmailer.io/reference/getlist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `brand_id` | path | `string` | yes | ID of the brand containing the list. |
| `list_id` | path | `string` | yes | ID of the list. |
