# Remove Contacts from List with Brevo

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/contacts/lists/:listId/contacts/remove`
- **Base URL:** `https://api.brevo.com`
- **Official documentation:** [Remove Contacts from List](https://developers.brevo.com/reference/remove-contact-from-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails` | body | `object<string>` | yes | Array of contact emails to remove from the list. |
| `listId` | path | `string` | yes | Brevo list ID. |
