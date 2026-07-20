# Update Space with GitBook

Updates an existing space in GitBook.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/spaces/:spaceId`
- **Base URL:** `https://api.gitbook.com/v1`
- **Official documentation:** [Update Space](https://gitbook.com/docs/developers/gitbook-api/api-reference/spaces)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `defaultLevel` | body | `string` | no | Default level applied to the space. |
| `editMode` | body | `string` | no | — |
| `emoji` | body | `string` | no | Emoji shown for the space. |
| `language` | body | `string` | no | — |
| `spaceId` | path | `string` | yes | — |
| `title` | body | `string` | no | Title of the space. Maximum length: 50. |
