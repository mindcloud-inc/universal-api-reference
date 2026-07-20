# List entries with Contentful

## Endpoint

- **Method:** `GET`
- **Path:** `/spaces/:spaceId/environments/:environmentId/entries`
- **Base URL:** `https://api.contentful.com`
- **Official documentation:** [List entries](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/entries/entries-collection/get-all-entries-of-a-space)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | Contentful space ID to query. |
| `environmentId` | path | `string` | yes | Contentful environment ID inside the selected space. |
| `content_type` | query | `string` | no | Return only entries for a specific content type ID. |
| `locale` | query | `string` | no | Locale code used to localize entry fields. |
| `include` | query | `number` | no | Linked-entry include depth from 0 to 10. |
| `select` | query | `string` | no | Comma-separated list of fields to include in the response. |
