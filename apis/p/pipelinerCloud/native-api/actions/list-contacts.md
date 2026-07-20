# List Contacts with Pipeliner Cloud

Retrieves contacts from Pipeliner Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/entities/Contacts`
- **Base URL:** `{serviceUrl}/api/v100/rest/spaces/{spaceId}`
- **Official documentation:** [List Contacts](https://pipelinercrm.eu.apidog.com/contacts-list-3640865e0)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include-deleted` | query | `boolean` | no | Include deleted records in the result set. |
| `expand` | query | `string` | no | Comma-separated related resources to expand. |
| `load-only` | query | `string` | no | Comma-separated fields to return. |
