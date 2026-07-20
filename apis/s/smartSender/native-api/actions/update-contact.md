# Update Contact with Smart Sender

Updates an existing contact in Smart Sender.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/contacts/:contactId`
- **Base URL:** `https://api.smartsender.com`
- **Official documentation:** [Update Contact](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676444281/Contacts%2BAPI%2B-%2Ben)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | The Smart Sender contact ID. |
| `values` | body | `string` | no | Key-value fields to update for the contact. |
