# Add Contact Funnel with Smart Sender

Adds a funnel subscription to a contact in Smart Sender.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contacts/:contactId/funnels/:serviceKey`
- **Base URL:** `https://api.smartsender.com`
- **Official documentation:** [Add Contact Funnel](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676444426/Contact%2BFunnels%2BAPI%2B-%2Ben)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | The Smart Sender contact ID. |
| `serviceKey` | path | `string` | yes | The funnel service key. |
