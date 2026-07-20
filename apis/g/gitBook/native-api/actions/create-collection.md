# Create Collection with GitBook

Creates a new collection in GitBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/orgs/:organizationId/collections`
- **Base URL:** `https://api.gitbook.com/v1`
- **Official documentation:** [Create Collection](https://gitbook.com/docs/developers/gitbook-api/api-reference/collections)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | — |
| `parent` | body | `string` | no | — |
| `title` | body | `string` | no | Title of the collection. Maximum length: 50. |
