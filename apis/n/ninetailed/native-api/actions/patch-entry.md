# Patch Entry with Ninetailed

## Endpoint

- **Method:** `PATCH`
- **Path:** `/spaces/:spaceId/environments/:environmentId/entries/:entryId`
- **Base URL:** `https://api.contentful.com`
- **Official documentation:** [Patch Entry](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/entries/entry)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | Contentful space ID. |
| `environmentId` | path | `string` | yes | Contentful environment ID, such as master. |
| `entryId` | path | `string` | yes | Entry ID to patch. |
| `version` | body | `number` | yes | Current Contentful entry version for X-Contentful-Version. |
| `patches[]` | body | `array<object>` | yes | JSON Patch operations to apply to the entry. |
