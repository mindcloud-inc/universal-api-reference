# Manage Contact Tags with Contacts+

Adds or removes tags on Contacts+ contacts.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/contacts.manageTags`
- **Base URL:** `https://api.contactsplus.com`
- **Official documentation:** [Manage Contact Tags](https://www.contactsplus.com/developers/contacts-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactIds[]` | body | `array<string>` | yes | The contact IDs whose tags should be changed. |
| `addTagIds[]` | body | `array<string>` | no | Tag IDs to add to the contacts. |
| `removeTagIds[]` | body | `array<string>` | no | Tag IDs to remove from the contacts. |
| `teamId` | body | `string` | no | Manage tags in this team instead of personal contacts. |
