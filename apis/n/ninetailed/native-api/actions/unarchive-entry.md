# Unarchive Entry with Ninetailed

## Endpoint

- **Method:** `DELETE`
- **Path:** `/spaces/:spaceId/environments/:environmentId/entries/:entryId/archived`
- **Base URL:** `https://api.contentful.com`
- **Official documentation:** [Unarchive Entry](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/entries/entry-archiving)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | Contentful space ID. |
| `environmentId` | path | `string` | yes | Contentful environment ID, such as master. |
| `entryId` | path | `string` | yes | Entry ID to unarchive. |
