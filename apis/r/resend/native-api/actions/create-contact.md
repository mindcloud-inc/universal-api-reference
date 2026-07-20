# Create Contact with Resend

Creates a new contact in Resend.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.resend.com`
- **Official documentation:** [Create Contact](https://resend.com/docs/api-reference/contacts/create-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | — |
| `id` | body | `string` | no | — |
| `subscription` | body | `string` | no | Accepted values: `opt_in` or `opt_out`. |
| `first_name` | body | `string` | no | — |
| `last_name` | body | `string` | no | — |
| `unsubscribed` | body | `boolean` | no | Sets the contact's global unsubscribe status. When true, the contact is unsubscribed from all broadcasts. |
| `properties` | body | `object` | no | Object map of custom contact properties as key/value pairs. |
| `segments[]` | body | `array<string>` | no | Array of segment IDs to add the contact to. |
| `topics[]` | body | `array<object>` | no | Array of topic subscription objects with `id` and `subscription` (`opt_in` or `opt_out`). |
