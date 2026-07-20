# Get Contact Gates with Smart Sender

Retrieves a contact's available communication channels from Smart Sender.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/contacts/:contactId/gates`
- **Base URL:** `https://api.smartsender.com`
- **Official documentation:** [Get Contact Gates](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676444281/Contacts%2BAPI%2B-%2Ben)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | The Smart Sender contact ID. |
