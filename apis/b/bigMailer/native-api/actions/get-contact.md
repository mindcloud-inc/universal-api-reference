# Get Contact with BigMailer

Retrieves a contact from a BigMailer brand.

## Endpoint

- **Method:** `GET`
- **Path:** `/brands/:brand_id/contacts/:contact_id`
- **Base URL:** `https://api.bigmailer.io/v1`
- **Official documentation:** [Get Contact](https://docs.bigmailer.io/reference/getcontact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `brand_id` | path | `string` | yes | ID of the brand containing the contact. |
| `contact_id` | path | `string` | yes | ID or email address of the contact. |
