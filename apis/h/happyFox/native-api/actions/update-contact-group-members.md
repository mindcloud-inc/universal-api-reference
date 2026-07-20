# Update Contact Group Members with HappyFox

Updates contacts in a HappyFox contact group.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact_group/:contact_group_id/update_contacts/`
- **Base URL:** `https://{accountDomain}/api/1.1/json`
- **Official documentation:** [Update Contact Group Members](https://support.happyfox.com/kb/article/1092-contacts-and-contact-groups-api-endpoints/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_group_id` | path | `string` | yes | HappyFox contact group ID. |
| `contacts[]` | body | `array<object>` | yes | — |
