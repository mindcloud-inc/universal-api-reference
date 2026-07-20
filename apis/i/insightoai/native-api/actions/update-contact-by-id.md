# Update Contact By Id with Insighto.ai

## Endpoint

- **Method:** `PUT`
- **Path:** `/contact/:contact_id`
- **Base URL:** `https://api.insighto.ai/api/v1`
- **Official documentation:** [Update Contact By Id](https://docs.insighto.ai/api-reference/contact/update-contact-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `string` | yes | The UUID id of the contact. |
| `first_name` | body | `string` | no | Contact first name. |
| `last_name` | body | `string` | no | Contact last name. |
| `email` | body | `string` | no | Contact email address. |
