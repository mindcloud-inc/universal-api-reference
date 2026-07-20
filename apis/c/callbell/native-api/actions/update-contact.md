# Update Contact with Callbell

Updates an existing contact in Callbell.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contacts/:uuid`
- **Base URL:** `https://api.callbell.eu/v1`
- **Official documentation:** [Update Contact](https://docs.callbell.eu/api/reference/contacts_api/patch_contacts/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assigned_user` | body | `string` | no | Collaborator email to assign to the contact. |
| `bot_status` | body | `string` | no | Bot status to apply to the contact. |
| `custom_fields` | body | `object` | no | Custom field values keyed by field name. |
| `name` | body | `string` | no | Updated display name for the contact. |
| `tags[]` | body | `array<string>` | no | List of existing Callbell tags to assign. |
| `team_uuid` | body | `string` | no | Team UUID to assign to the contact. |
| `unassign_user` | body | `boolean` | no | Remove the assigned collaborator from the contact. |
| `uuid` | path | `string` | yes | Unique identifier of the contact to update. |
