# Create Tree Folder with Documenterra

Creates a page tree folder in Documenterra.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/toc/nodes`
- **Base URL:** `https://mindclouddocumenterra.try.documenterra.net/api/v1`
- **Official documentation:** [Create Tree Folder](https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-sozdaniye-elementa-dereva-stranits-papki)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `caption` | body | `string` | yes | Tree folder caption. |
| `isShowInToc` | body | `boolean` | no | Whether to show the folder in the tree of contents. |
| `ordinalNo` | body | `number` | no | Optional folder order index. |
| `parentId` | body | `string` | no | Optional parent tree node identifier. |
| `projectId` | path | `string` | yes | Documenterra project identifier. |
