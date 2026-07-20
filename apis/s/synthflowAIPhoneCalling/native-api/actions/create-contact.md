# Create Contact with Synthflow AI Phone Calling

Creates a new contact in Synthflow.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.synthflow.ai/v2`
- **Official documentation:** [Create Contact](https://docs.synthflow.ai/api-reference/platform-api/contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_metadata` | body | `object` | no | Additional metadata for the contact. |
| `email` | body | `string` | no | The contact's email address. |
| `name` | body | `string` | yes | The contact's name. |
| `phone_number` | body | `string` | yes | The contact's phone number in E.164 format. |
