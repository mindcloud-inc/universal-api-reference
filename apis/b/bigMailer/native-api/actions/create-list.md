# Create List with BigMailer

Creates a new list in a BigMailer brand.

## Endpoint

- **Method:** `POST`
- **Path:** `/brands/:brand_id/lists`
- **Base URL:** `https://api.bigmailer.io/v1`
- **Official documentation:** [Create List](https://docs.bigmailer.io/reference/createlist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `brand_id` | path | `string` | yes | ID of the brand to create the list in. |
| `name` | body | `string` | yes | Name of the list. |
