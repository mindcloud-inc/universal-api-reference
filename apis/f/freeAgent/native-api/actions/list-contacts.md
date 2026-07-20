# List Contacts with FreeAgent

Retrieves a list of contacts from FreeAgent.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://api.freeagent.com/v2`
- **Official documentation:** [List Contacts](https://dev.freeagent.com/docs/contacts#list-all-contacts)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `view` | query | `string` | no | Return all, active, hidden, clients, suppliers, bank accounts, employees, or projects contacts. |
| `updated_since` | query | `date` | no | Only return contacts updated since this ISO 8601 timestamp. |
