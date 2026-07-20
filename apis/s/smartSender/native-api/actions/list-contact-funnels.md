# List Contact Funnels with Smart Sender

Retrieves funnel subscriptions for a contact in Smart Sender.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/contacts/:contactId/funnels`
- **Base URL:** `https://api.smartsender.com`
- **Official documentation:** [List Contact Funnels](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676444426/Contact%2BFunnels%2BAPI%2B-%2Ben)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | The Smart Sender contact ID. |
