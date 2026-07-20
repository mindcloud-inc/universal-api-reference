# Create Page with Coda

Creates a new page in a Coda doc.

## Endpoint

- **Method:** `POST`
- **Path:** `/docs/:docId/pages`
- **Base URL:** `https://coda.io/apis/v1`
- **Official documentation:** [Create Page](https://coda.io/developers/apis/v1#tag/Pages/operation/createPage)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `docId` | path | `list` | yes |
| `name` | body | `string` | no |
| `subtitle` | body | `string` | no |
| `iconName` | body | `string` | no |
| `imageUrl` | body | `string` | no |
| `parentPageId` | body | `string` | no |
| `pageContent` | body | `object` | no |
| `pageContent.type` | body | `string` | no |
| `pageContent.canvasContent` | body | `object` | no |
| `pageContent.canvasContent.format` | body | `string` | no |
| `pageContent.canvasContent.content` | body | `string` | no |
| `pageContent.url` | body | `string` | no |
| `pageContent.renderMethod` | body | `string` | no |
| `pageContent.mode` | body | `string` | no |
| `pageContent.includeSubpages` | body | `boolean` | no |
| `pageContent.sourcePageId` | body | `string` | no |
| `pageContent.sourceDocId` | body | `string` | no |
