# Update Collection with GitBook

Updates an existing collection in GitBook.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/collections/:collectionId`
- **Base URL:** `https://api.gitbook.com/v1`
- **Official documentation:** [Update Collection](https://gitbook.com/docs/developers/gitbook-api/api-reference/collections)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | — |
| `defaultLevel` | body | `string` | no | Default level applied to the collection. |
| `description` | body | `string` | no | Description of the collection. Maximum length: 100. |
| `title` | body | `string` | no | Title of the collection. Maximum length: 50. |
