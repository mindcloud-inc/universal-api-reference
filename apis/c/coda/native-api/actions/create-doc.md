# Create Doc with Coda

Creates a new doc in Coda.

## Endpoint

- **Method:** `POST`
- **Path:** `/docs`
- **Base URL:** `https://coda.io/apis/v1`
- **Official documentation:** [Create Doc](https://coda.io/developers/apis/v1#tag/Docs/operation/createDoc)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `title` | body | `string` | no |
| `sourceDoc` | body | `string` | no |
| `timezone` | body | `string` | no |
| `folderId` | body | `string` | no |
| `initialPage` | body | `object` | no |
| `initialPage.name` | body | `string` | no |
| `initialPage.subtitle` | body | `string` | no |
| `initialPage.iconName` | body | `string` | no |
| `initialPage.imageUrl` | body | `string` | no |
| `initialPage.parentPageId` | body | `string` | no |
| `initialPage.pageContent` | body | `object` | no |
| `initialPage.pageContent.type` | body | `string` | no |
| `initialPage.pageContent.canvasContent` | body | `object` | no |
| `initialPage.pageContent.canvasContent.format` | body | `string` | no |
| `initialPage.pageContent.canvasContent.content` | body | `string` | no |
| `initialPage.pageContent.url` | body | `string` | no |
| `initialPage.pageContent.renderMethod` | body | `string` | no |
| `initialPage.pageContent.mode` | body | `string` | no |
| `initialPage.pageContent.includeSubpages` | body | `boolean` | no |
| `initialPage.pageContent.sourcePageId` | body | `string` | no |
| `initialPage.pageContent.sourceDocId` | body | `string` | no |
