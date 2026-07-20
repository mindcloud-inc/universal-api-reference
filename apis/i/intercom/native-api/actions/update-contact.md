# Update Contact with Intercom

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:contact_id`
- **Base URL:** `https://api.intercom.io`
- **Official documentation:** [Update Contact](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/contacts/updatecontact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `string` | yes | Intercom contact identifier |
| `role` | body | `string` | no | The role of the contact |
| `external_id` | body | `string` | no | A unique identifier for the contact provided by your system |
| `email` | body | `string` | no | The contact email address |
| `phone` | body | `string` | no | The contact phone number |
| `name` | body | `string` | no | The contact name |
| `avatar` | body | `string` | no | An image URL containing the contact avatar |
| `signed_up_at` | body | `number` | no | Unix timestamp for when the contact signed up |
| `last_seen_at` | body | `number` | no | Unix timestamp for when the contact was last seen |
| `owner_id` | body | `number` | no | The admin assigned as contact owner |
| `unsubscribed_from_emails` | body | `boolean` | no | Whether the contact is unsubscribed from emails |
| `custom_attributes` | body | `object` | no | Custom attributes to set on the contact |
