# Create Contact Message with Cliengo

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/:contactId/messages`
- **Base URL:** `https://api.cliengo.com/1.0`
- **Official documentation:** [Create Contact Message](https://developers.cliengo.com/reference/contactscontactidmessages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | Identifier of the Cliengo contact. |
| `message` | body | `string` | yes | Message to add to the contact. |
