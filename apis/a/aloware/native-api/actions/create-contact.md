# Create Contact with Aloware

Creates a new contact in Aloware.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/webhook/forms`
- **Base URL:** `https://app.aloware.com`
- **Official documentation:** [Create Contact](https://support.aloware.com/en/articles/9020058-aloware-lead-api-documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phone_number` | body | `string` | yes | Primary phone number for the contact. |
| `name` | body | `string` | no | Full contact name. |
| `email` | body | `string` | no | Contact email address. |
| `company_name` | body | `string` | no | Company name for the contact. |
| `user_id` | body | `string` | no | Assign the contact to a specific user. |
| `ring_group_id` | body | `string` | no | Assign the contact through a ring group. |
| `notes` | body | `string` | no | Notes to save on the contact. |
| `sequence_id` | body | `string` | no | Optional sequence to enroll the contact into. |
