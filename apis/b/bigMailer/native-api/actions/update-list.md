# Update List with BigMailer

Updates an existing list in a BigMailer brand.

## Endpoint

- **Method:** `POST`
- **Path:** `/brands/:brand_id/lists/:list_id`
- **Base URL:** `https://api.bigmailer.io/v1`
- **Official documentation:** [Update List](https://docs.bigmailer.io/reference/updatelist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `brand_id` | path | `string` | yes | ID of the brand containing the list. |
| `list_id` | path | `string` | yes | ID of the list. |
| `name` | body | `string` | no | Updated name of the list. |
