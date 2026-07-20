# Update Contact with BigMailer

Updates an existing contact in a BigMailer brand.

## Endpoint

- **Method:** `POST`
- **Path:** `/brands/:brand_id/contacts/:contact_id`
- **Base URL:** `https://api.bigmailer.io/v1`
- **Official documentation:** [Update Contact](https://docs.bigmailer.io/reference/updatecontact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `brand_id` | path | `string` | yes | ID of the brand containing the contact. |
| `contact_id` | path | `string` | yes | ID or email address of the contact. |
| `field_values_op` | query | `string` | no | How field values should be applied. |
| `list_ids_op` | query | `string` | no | How list IDs should be applied. |
| `unsubscribe_ids_op` | query | `string` | no | How unsubscribe IDs should be applied. |
| `email` | body | `string` | no | Email address of the contact. |
| `field_values[]` | body | `array<object>` | no | Field values to save with the contact. |
| `list_ids[]` | body | `array<string>` | no | IDs of lists the contact should be added to. |
| `unsubscribe_all` | body | `boolean` | no | Unsubscribe the contact from all message types. |
| `unsubscribe_ids[]` | body | `array<string>` | no | IDs of message types the contact should be unsubscribed from. |
