# List Folder Items with Canva

Retrieves items in a Canva folder.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/folders/:folderId/items`
- **Base URL:** `https://api.canva.com/rest`
- **Official documentation:** [List Folder Items](https://www.canva.dev/docs/connect/api-reference/folders/list-folder-items/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | path | `string` | yes | Maximum length: 50. |
| `item_types` | query | `list<string>` | no | Accepted values: `design`, `folder`, `image`. Send multiple values as a string separated by `,`. |
| `sort_by` | query | `list` | no | Accepted values: `created_ascending`, `created_descending`, `modified_ascending`, `modified_descending`, `title_ascending`, `title_descending`. |
| `pin_status` | query | `list` | no | Accepted values: `any`, `pinned`. |
| `continuation` | query | `string` | no | — |
