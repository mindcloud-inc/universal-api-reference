# Update Contact with Nimble

Updates an existing contact in Nimble.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/contact/:contact_id`
- **Base URL:** `https://app.nimble.com`
- **Official documentation:** [Update Contact](https://www.nimble.com/developers/docs/#tag/Contacts/operation/put-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `string` | yes | Nimble contact_id path parameter. |
| `record_type` | body | `string` | no | — |
| `fields` | body | `object` | no | — |
| `is_important` | body | `boolean` | no | — |
