# List Contacts with Anabix CRM

Retrieves contact records from Anabix CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `https://app.anabix.cz`
- **Official documentation:** [List Contacts](https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | body | `number` | no | Maximum number of records to return. Anabix documents 200 as the standard maximum. |
| `offset` | body | `number` | no | Number of records to skip. |
| `criteria` | body | `object` | no | Filter object keyed by Anabix contact fields, for example email or lastName. |
| `includeMetadata` | body | `number` | no | Set to 1 to include total record metadata for pagination. |
