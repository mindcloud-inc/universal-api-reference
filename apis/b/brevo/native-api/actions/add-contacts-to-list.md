# Add Contacts to List with Brevo

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/contacts/lists/:listId/contacts/add`
- **Base URL:** `https://api.brevo.com`
- **Official documentation:** [Add Contacts to List](https://developers.brevo.com/reference/add-contact-to-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails` | body | `object<string>` | yes | Array of contact emails to add to the list. Send multiple values as a array. |
| `ids` | body | `list<number>` | no | Array of contact IDs to add to the list. |
| `listId` | path | `string` | yes | Brevo list ID. |
