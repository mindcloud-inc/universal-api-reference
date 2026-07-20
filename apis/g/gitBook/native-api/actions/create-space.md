# Create Space with GitBook

Creates a new space in GitBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/orgs/:organizationId/spaces`
- **Base URL:** `https://api.gitbook.com/v1`
- **Official documentation:** [Create Space](https://gitbook.com/docs/developers/gitbook-api/api-reference/spaces)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `editMode` | body | `string` | no | — |
| `emoji` | body | `string` | no | — |
| `language` | body | `string` | no | — |
| `organizationId` | path | `string` | yes | — |
| `parent` | body | `string` | no | — |
| `title` | body | `string` | no | Title of the space. Maximum length: 50. |
