# Delete Environment with Ninetailed

## Endpoint

- **Method:** `DELETE`
- **Path:** `/spaces/:spaceId/environments/:environmentId`
- **Base URL:** `https://api.contentful.com`
- **Official documentation:** [Delete Environment](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/environments/environment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | Contentful space ID. |
| `environmentId` | path | `string` | yes | Environment ID to delete. Use an isolated non-master environment only. |
