# List Items with DatoCMS

## Endpoint

- **Method:** `GET`
- **Path:** `/items`
- **Base URL:** `https://site-api.datocms.com`
- **Official documentation:** [List Items](https://www.datocms.com/docs/content-management-api/resources/item/instances)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[query]` | query | `string` | no | Text query applied to searchable fields. |
| `filter[type]` | query | `string` | no | Filter items by item type ID. |
| `locale` | query | `string` | no | Locale used for localized filtering and ordering. |
| `nested` | query | `boolean` | no | Include nested objects in the response payload when available. |
| `version` | query | `string` | no | Select content version, for example current or published. |
| `filter[ids]` | query | `string` | no | Comma-separated item IDs to return. |
| `filter[only_valid]` | query | `string` | no | When set, only valid records are returned. |
