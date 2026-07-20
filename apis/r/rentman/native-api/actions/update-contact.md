# Update Contact with Rentman

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:id`
- **Base URL:** `https://api.rentman.net`
- **Official documentation:** [Update Contact](https://api.rentman.net/#operation/updateContact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric ID of the contact to update. |
| `name` | body | `string` | no | Contact name. |
| `type` | body | `string` | no | Contact type: private or company. |
| `email_1` | body | `string` | no | Primary email address. |
| `phone_1` | body | `string` | no | Primary phone number. |
| `mailing_city` | body | `string` | no | Mailing city. |
