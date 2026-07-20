# Update Contact with Ellipsend

Updates a contact in Ellipsend by token.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contact/[:token]`
- **Base URL:** `https://api.ellipsend.com/v1`
- **Official documentation:** [Update Contact](https://api.ellipsend.com/v1/docs#/Contact/put_contact__token_)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `token` | path | `string` | yes | The contact token. |
| `status_id` | body | `number` | no | ID of the status to assign. |
| `label_id` | body | `number` | no | ID of the label to assign. |
| `assignee_id` | body | `number` | no | ID of the assignee to assign. |
| `first_name` | body | `string` | no | Contact's first name. |
| `last_name` | body | `string` | no | Contact's last name. |
| `email` | body | `string` | no | Contact's email address. |
| `phone` | body | `string` | no | Contact's phone number. |
| `address` | body | `string` | no | Contact's physical address. |
| `city` | body | `string` | no | Contact's city. |
| `state` | body | `string` | no | Contact's state or province. |
| `postal_code` | body | `string` | no | Contact's postal or zip code. |
| `country` | body | `string` | no | Contact's country. |
| `company` | body | `string` | no | Contact's company name. |
| `title` | body | `string` | no | Contact's job title. |
| `custom_fields` | body | `object` | no | Additional custom fields for the contact. |
