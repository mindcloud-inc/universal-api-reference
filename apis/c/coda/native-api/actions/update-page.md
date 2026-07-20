# Update Page with Coda

Updates a page in a Coda doc.

## Endpoint

- **Method:** `PUT`
- **Path:** `/docs/:docId/pages/:pageIdOrName`
- **Base URL:** `https://coda.io/apis/v1`
- **Official documentation:** [Update Page](https://coda.io/developers/apis/v1#tag/Pages/operation/updatePage)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `docId` | path | `list` | yes |
| `pageIdOrName` | path | `list` | yes |
| `name` | body | `string` | no |
| `subtitle` | body | `string` | no |
| `iconName` | body | `string` | no |
| `imageUrl` | body | `string` | no |
| `isHidden` | body | `boolean` | no |
| `contentUpdate` | body | `object` | no |
| `contentUpdate.insertionMode` | body | `string` | no |
| `contentUpdate.elementId` | body | `string` | no |
| `contentUpdate.canvasContent` | body | `object` | no |
| `contentUpdate.canvasContent.format` | body | `string` | no |
| `contentUpdate.canvasContent.content` | body | `string` | no |
