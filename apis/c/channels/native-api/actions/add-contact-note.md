# Add Contact Note with Channels

Creates a contact note in Channels.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/contacts/{contactId}/note`
- **Base URL:** `https://api.channels.app`
- **Official documentation:** [Add Contact Note](https://developers.channels.app/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `number` | yes | Contact ID to add the note to. |
| `note` | body | `string` | yes | Contents of the note. |
