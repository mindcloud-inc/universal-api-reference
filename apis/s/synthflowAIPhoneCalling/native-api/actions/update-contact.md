# Update Contact with Synthflow AI Phone Calling

Updates an existing contact in Synthflow.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contacts/:contact_id`
- **Base URL:** `https://api.synthflow.ai/v2`
- **Official documentation:** [Update Contact](https://docs.synthflow.ai/api-reference/platform-api/contacts/update-a-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `string` | yes | The Synthflow contact identifier. |
| `contact_metadata` | body | `object` | no | Update additional metadata for the contact. |
| `email` | body | `string` | no | Update the contact's email address. |
| `name` | body | `string` | no | Update the contact's name. |
| `phone_number` | body | `string` | no | Update the contact's phone number in E.164 format. |
