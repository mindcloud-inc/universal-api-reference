# List Contacts with Clio Grow

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://api.clio.com/grow`
- **Official documentation:** [List Contacts](https://docs.developers.clio.com/clio-grow/api-reference/#tag/Contacts/operation/Contact%23index)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Search across contact names, emails, and phone numbers. |
| `created_since` | query | `date` | no | Only include contacts created on or after this ISO-8601 timestamp. |
| `updated_since` | query | `date` | no | Only include contacts updated on or after this ISO-8601 timestamp. |
