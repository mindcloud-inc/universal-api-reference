# Update Contact with Salesflare

## Endpoint

- **Method:** `PUT`
- **Path:** `contacts/:contact_id`
- **Base URL:** `https://api.salesflare.com`
- **Official documentation:** [Update Contact](https://api.salesflare.com/docs#/Contacts/putContactsContact_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `number` | yes | The Salesflare contact ID. |
| `email` | body | `string` | no | The contact email address. |
| `name` | body | `string` | no | The full name of the contact. |
