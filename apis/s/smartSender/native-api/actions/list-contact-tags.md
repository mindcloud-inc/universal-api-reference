# List Contact Tags with Smart Sender

Retrieves tags for a contact in Smart Sender.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/contacts/:contactId/tags`
- **Base URL:** `https://api.smartsender.com`
- **Official documentation:** [List Contact Tags](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/97386531/Contact%2BTags%2BAPI)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | The Smart Sender contact ID. |
