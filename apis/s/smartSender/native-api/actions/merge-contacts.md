# Merge Contacts with Smart Sender

Merges one contact into another in Smart Sender.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contacts/:contactId/unite/:targetContactId`
- **Base URL:** `https://api.smartsender.com`
- **Official documentation:** [Merge Contacts](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676444281/Contacts%2BAPI%2B-%2Ben)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | The primary Smart Sender contact ID. |
| `targetContactId` | path | `string` | yes | The contact ID to merge into the primary contact. |
