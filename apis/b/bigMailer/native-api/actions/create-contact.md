# Create Contact with BigMailer

Creates a new contact in a BigMailer brand.

## Endpoint

- **Method:** `POST`
- **Path:** `/brands/:brand_id/contacts`
- **Base URL:** `https://api.bigmailer.io/v1`
- **Official documentation:** [Create Contact](https://docs.bigmailer.io/reference/createcontact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `brand_id` | path | `string` | yes | ID of the brand to create the contact in. |
| `validate` | query | `boolean` | no | Validate email deliverability before adding the contact. |
| `email` | body | `string` | yes | Email address of the contact. |
| `field_values[]` | body | `array<object>` | no | Field values to save with the contact. |
| `list_ids[]` | body | `array<string>` | no | IDs of lists the contact should be added to. |
| `unsubscribe_all` | body | `boolean` | no | Unsubscribe the contact from all future campaigns. |
| `unsubscribe_ids[]` | body | `array<string>` | no | IDs of message types the contact should be unsubscribed from. |
