# Create Contact with Wooxy

Creates a new contact in Wooxy.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/contacts/add`
- **Base URL:** `https://api.wooxy.com`
- **Official documentation:** [Create Contact](https://wooxy.com/api-documentation/contacts/add-new-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactListId` | body | `string` | yes | Wooxy contact list ID. |
| `contacts[]` | body | `array<object>` | yes | Array of contact objects to create. |
| `webHookUri` | body | `string` | no | Optional callback URL for async status notifications. |
