# Update Contact with Planfix

Updates an existing contact or company in Planfix.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact/:id`
- **Base URL:** `{accountBaseUrl}/rest`
- **Official documentation:** [Update Contact](https://help.planfix.com/restapidocs/#/Contact/post-contact-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Planfix contact identifier. |
| `name` | body | `string` | no | Updated contact name. |
| `email` | body | `string` | no | Updated primary email address. |
| `description` | body | `string` | no | Updated contact description. |
