# Update Contact with Oneflow

Updates an existing contact in Oneflow.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:id`
- **Base URL:** `https://api.oneflow.com/v1`
- **Official documentation:** [Update Contact](https://developer.oneflow.com/reference/update-a-contact-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Oneflow contact ID. |
| `name` | body | `string` | no | The contact name. |
| `email` | body | `string` | no | The contact email. |
| `company_name` | body | `string` | no | The contact company name. |
| `phone_number` | body | `string` | no | The contact phone number. |
| `notes` | body | `string` | no | Notes for the contact. |
