# Update Tree Element with Documenterra

Updates an existing page tree element in Documenterra.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:projectId/toc/nodes/:tocNodeId`
- **Base URL:** `https://mindclouddocumenterra.try.documenterra.net/api/v1`
- **Official documentation:** [Update Tree Element](https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-obnovleniye-elementa-dereva-stranits)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `caption` | body | `string` | yes | Updated tree node caption. |
| `isShowInToc` | body | `boolean` | no | Whether to show the node in the tree of contents. |
| `ordinalNo` | body | `number` | no | Updated node order index. |
| `parentId` | body | `string` | no | Updated parent tree node identifier. |
| `projectId` | path | `string` | yes | Documenterra project identifier. |
| `tocNodeId` | path | `string` | yes | Documenterra tree node identifier. |
| `updatedFields` | body | `string` | yes | Comma-separated list of tree fields to update. |
