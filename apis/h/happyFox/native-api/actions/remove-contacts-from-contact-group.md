# Remove Contacts from Contact Group with HappyFox

Removes contacts from a HappyFox contact group.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact_group/:contact_group_id/delete_contacts/`
- **Base URL:** `https://{accountDomain}/api/1.1/json`
- **Official documentation:** [Remove Contacts from Contact Group](https://support.happyfox.com/kb/article/1092-contacts-and-contact-groups-api-endpoints/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_group_id` | path | `string` | yes | HappyFox contact group ID. |
| `contacts[]` | body | `array<number>` | yes | List of HappyFox contact IDs to remove from the group. |
