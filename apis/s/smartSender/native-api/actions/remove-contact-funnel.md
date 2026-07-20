# Remove Contact Funnel with Smart Sender

Removes a funnel subscription from a contact in Smart Sender.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/contacts/:contactId/funnels/:serviceKey`
- **Base URL:** `https://api.smartsender.com`
- **Official documentation:** [Remove Contact Funnel](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676444426/Contact%2BFunnels%2BAPI%2B-%2Ben)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | The Smart Sender contact ID. |
| `serviceKey` | path | `string` | yes | The funnel service key. |
