# Update Contact with Resend

Updates an existing contact in Resend.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contacts/:id`
- **Base URL:** `https://api.resend.com`
- **Official documentation:** [Update Contact](https://resend.com/docs/api-reference/contacts/update-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | path | `list<string>` | no | — |
| `first_name` | body | `string` | no | — |
| `id` | path | `string<string>` | yes | — |
| `last_name` | body | `string` | no | — |
| `unsubscribed` | body | `boolean` | no | If set to true, the contact will be unsubscribed from all Broadcasts. |
| `properties` | body | `object` | no | A map of custom property key-value pairs to update on the contact. |
