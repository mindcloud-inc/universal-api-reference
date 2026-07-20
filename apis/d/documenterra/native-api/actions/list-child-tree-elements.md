# List Child Tree Elements with Documenterra

Retrieves child page tree elements from Documenterra.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/toc/nodes/:tocNodeId/children`
- **Base URL:** `https://mindclouddocumenterra.try.documenterra.net/api/v1`
- **Official documentation:** [List Child Tree Elements](https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-polucheniye-dochernikh-elementov-dereva-stranits)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `isRecursive` | query | `boolean` | no | Whether to fetch descendants recursively. |
| `projectId` | path | `string` | yes | Documenterra project identifier. |
| `tocNodeId` | path | `string` | yes | Documenterra parent tree node identifier. |
