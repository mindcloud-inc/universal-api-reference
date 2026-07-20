# List Uploads with DatoCMS

## Endpoint

- **Method:** `GET`
- **Path:** `/uploads`
- **Base URL:** `https://site-api.datocms.com`
- **Official documentation:** [List Uploads](https://www.datocms.com/docs/content-management-api/resources/upload/instances)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[query]` | query | `string` | no | Textual query used to search uploads. |
| `filter[ids]` | query | `string` | no | Comma-separated upload IDs to fetch. |
| `filter[locale]` | query | `string` | no | Locale used when text query or field filters are provided. |
