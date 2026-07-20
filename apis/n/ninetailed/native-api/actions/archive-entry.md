# Archive Entry with Ninetailed

## Endpoint

- **Method:** `PUT`
- **Path:** `/spaces/:spaceId/environments/:environmentId/entries/:entryId/archived`
- **Base URL:** `https://api.contentful.com`
- **Official documentation:** [Archive Entry](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/entries/entry-archiving)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | Contentful space ID. |
| `environmentId` | path | `string` | yes | Contentful environment ID, such as master. |
| `entryId` | path | `string` | yes | Entry ID to archive. |
| `version` | body | `number` | yes | Current Contentful entry version for X-Contentful-Version. |
