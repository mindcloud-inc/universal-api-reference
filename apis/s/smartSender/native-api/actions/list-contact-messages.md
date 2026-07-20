# List Contact Messages with Smart Sender

Retrieves messages for a contact in Smart Sender.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/contacts/:contactId/messages`
- **Base URL:** `https://api.smartsender.com`
- **Official documentation:** [List Contact Messages](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676575830/Messages%2BAPI%2B-%2Ben)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `activities` | query | `boolean` | no | Whether to include system messages in the results. |
| `contactId` | path | `string` | yes | The Smart Sender contact ID. |
