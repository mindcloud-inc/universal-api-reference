# Delete Contact with Wooxy

Deletes an existing contact from Wooxy.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/contacts/remove`
- **Base URL:** `https://api.wooxy.com`
- **Official documentation:** [Delete Contact](https://wooxy.com/api-documentation/contacts/remove-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactListId` | body | `string` | yes | Wooxy contact list ID. |
| `emails[]` | body | `array<string>` | no | Array of emails to remove. |
| `phoneNumbers[]` | body | `array<string>` | no | Array of phone numbers to remove. |
| `userIds[]` | body | `array<string>` | no | Array of user IDs to remove. |
| `webHookUri` | body | `string` | no | Optional callback URL for async status notifications. |
