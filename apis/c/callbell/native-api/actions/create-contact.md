# Create Contact with Callbell

Creates a new contact in Callbell.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.callbell.eu/v1`
- **Official documentation:** [Create Contact](https://docs.callbell.eu/api/reference/contacts_api/post_contacts/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assigned_user` | body | `string` | no | Collaborator email to assign to the contact. |
| `bot_status` | body | `string` | no | Bot status to apply to the contact. |
| `channel_uuid` | body | `string` | no | Channel UUID to associate with the contact. |
| `custom_fields` | body | `object` | no | Custom field values keyed by field name. |
| `identifier` | body | `string` | yes | Phone number or platform identifier for the contact. |
| `name` | body | `string` | yes | Display name for the contact. |
| `source` | body | `string` | yes | Source of the contact, such as whatsapp. |
| `tags[]` | body | `array<string>` | no | List of existing Callbell tags to assign. |
| `team_uuid` | body | `string` | no | Team UUID to assign to the contact. |
