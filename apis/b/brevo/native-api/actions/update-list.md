# Update List with Brevo

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/contacts/lists/:listId`
- **Base URL:** `https://api.brevo.com`
- **Official documentation:** [Update List](https://developers.brevo.com/reference/update-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `string` | yes | Brevo list ID. |
| `name` | body | `string` | yes | New list name. |
