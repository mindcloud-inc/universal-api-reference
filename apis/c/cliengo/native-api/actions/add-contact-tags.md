# Add Contact Tags with Cliengo

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/:contactId/tags`
- **Base URL:** `https://api.cliengo.com/1.0`
- **Official documentation:** [Add Contact Tags](https://developers.cliengo.com/reference/contactscontactidtags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | Identifier of the Cliengo contact. |
| `tag` | body | `string` | yes | Tag to add to the contact. |
