# Create Page with Documenterra

Creates a page in Documenterra.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/articles`
- **Base URL:** `https://mindclouddocumenterra.try.documenterra.net/api/v1`
- **Official documentation:** [Create Page](https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-sozdaniye-stranitsy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assigneeUserName` | body | `string` | yes | Optional assignee username. |
| `body` | body | `string` | no | Page content body. |
| `id` | body | `string` | yes | Optional page identifier to assign during creation. |
| `indexKeywords[]` | body | `array<string>` | no | Optional page index keywords. |
| `isShowInToc` | body | `boolean` | no | Whether to show the page in the tree of contents. |
| `ownerUserName` | body | `string` | yes | Optional owner username. |
| `parentTocNodeId` | body | `string` | no | Optional parent tree node identifier. |
| `projectId` | path | `string` | yes | Documenterra project identifier. |
| `statusName` | body | `string` | yes | Optional Documenterra status name. |
| `title` | body | `string` | no | Page title. |
| `tocNodeCaption` | body | `string` | no | Optional tree caption for the page node. |
| `tocNodeOrdinalNo` | body | `number` | no | Optional tree order index for the page node. |
