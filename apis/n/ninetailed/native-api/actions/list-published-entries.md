# List Published Entries with Ninetailed

## Endpoint

- **Method:** `GET`
- **Path:** `/spaces/:space_id/environments/:environment_id/public/entries`
- **Base URL:** `https://api.contentful.com`
- **Official documentation:** [List Published Entries](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/entries/published-entries-collection)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `space_id` | path | `string` | yes | Contentful space ID. |
| `environment_id` | path | `string` | yes | Contentful environment ID. |
