# Add Handbook Item with Blaze AI

Creates a handbook item in Blaze AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/w/:workspace_id/handbooks/:handbook_id/items`
- **Base URL:** `https://api.blaze.ai`
- **Official documentation:** [Add Handbook Item](https://api.blaze.ai/api/documentation#!/handbook%20items/postApiV1WWorkspaceIdHandbooksHandbookIdItems)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes |
| `handbook_id` | path | `number` | yes |
| `handbook_item[type]` | body | `string` | yes |
| `handbook_item[position]` | body | `number` | no |
| `handbook_item[parent_item_id]` | body | `string` | no |
| `handbook_item[doc_id]` | body | `number` | yes |
| `handbook_item[title]` | body | `string` | yes |
| `handbook_item[url]` | body | `string` | yes |
