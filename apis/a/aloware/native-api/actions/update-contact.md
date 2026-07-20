# Update Contact with Aloware

Updates an existing contact in Aloware.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/webhook/forms`
- **Base URL:** `https://app.aloware.com`
- **Official documentation:** [Update Contact](https://support.aloware.com/en/articles/9020058-aloware-lead-api-documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_name` | body | `string` | no | Updated company name. |
| `email` | body | `string` | no | Updated contact email address. |
| `name` | body | `string` | no | Updated full contact name. |
| `notes` | body | `string` | no | Updated notes to save on the contact. |
| `phone_number` | body | `string` | yes | Primary phone number for the contact to update. |
| `ring_group_id` | body | `string` | no | Assign the contact through a ring group. |
| `user_id` | body | `string` | no | Assign the contact to a specific user. |
