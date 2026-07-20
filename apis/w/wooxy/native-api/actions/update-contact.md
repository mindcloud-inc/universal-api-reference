# Update Contact with Wooxy

Updates an existing contact in Wooxy.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/contacts/update`
- **Base URL:** `https://api.wooxy.com`
- **Official documentation:** [Update Contact](https://wooxy.com/api-documentation/contacts/update-contact-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactListId` | body | `string` | yes | Wooxy contact list ID. |
| `contacts[]` | body | `array<object>` | yes | Array of contact objects to update. Each item must include the required contact field set to the unique identifier you want to update (email, phoneNumber, or userId). |
| `upsert` | body | `boolean` | no | Create the contact if it does not already exist. |
| `webHookUri` | body | `string` | no | Optional callback URL for async status notifications. |
