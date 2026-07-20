# Delete Tree Element with Documenterra

Deletes an existing page tree element from Documenterra.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:projectId/toc/nodes/:tocNodeId`
- **Base URL:** `https://mindclouddocumenterra.try.documenterra.net/api/v1`
- **Official documentation:** [Delete Tree Element](https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-udaleniye-elementa-dereva-stranits)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Documenterra project identifier. |
| `tocNodeId` | path | `string` | yes | Documenterra tree node identifier. |
