# Add Contact Tags with TxtSync

Adds tags to a contact in TxtSync.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/:id/tags`
- **Base URL:** `https://api.txtsync.com`
- **Official documentation:** [Add Contact Tags](https://docs.txtsync.com/#create-tag-contact-associations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Contact identifier. |
| `TagIDs` | body | `list<number>` | yes | Tag identifiers to associate to the contact. Send multiple values as a array. |
