# Fire Contact Event with Smart Sender

Triggers an event for a contact in Smart Sender.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contacts/:contactId/fire`
- **Base URL:** `https://api.smartsender.com`
- **Official documentation:** [Fire Contact Event](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676444281/Contacts%2BAPI%2B-%2Ben)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | The Smart Sender contact ID. |
| `name` | body | `string` | yes | Case-sensitive event name to trigger. |
