# Import Contacts with Emailchef

Imports contacts into an Emailchef list.

## Endpoint

- **Method:** `POST`
- **Path:** `lists/:list_id/import`
- **Base URL:** `https://app.emailchef.com/apps/api/v1`
- **Official documentation:** [Import Contacts](https://emailchef.com/integration/#/Import/importContacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | path | `string` | yes | The Emailchef list ID. |
| `instance_in.contacts[]` | body | `array<array>` | no | — |
| `instance_in.notification_link` | body | `string` | no | — |
