# Search Contacts with Smart Sender

Finds contacts in Smart Sender by keyword.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/contacts/search`
- **Base URL:** `https://api.smartsender.com`
- **Official documentation:** [Search Contacts](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676444281/Contacts%2BAPI%2B-%2Ben)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `term` | query | `string` | no | Keyword used to search contacts. |
