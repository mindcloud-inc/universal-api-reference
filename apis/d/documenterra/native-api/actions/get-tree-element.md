# Get Tree Element with Documenterra

Retrieves a page tree element from Documenterra.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/toc/nodes/:nodeId`
- **Base URL:** `https://mindclouddocumenterra.try.documenterra.net/api/v1`
- **Official documentation:** [Get Tree Element](https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-polucheniye-elementa-dereva-stranits)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `nodeId` | path | `string` | yes | Documenterra tree node identifier. |
| `projectId` | path | `string` | yes | Documenterra project identifier. |
