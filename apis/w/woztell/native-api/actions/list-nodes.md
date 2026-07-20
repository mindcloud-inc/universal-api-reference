# List Nodes with Woztell

Retrieves nodes from your Woztell workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://open.api.woztell.com/v3`
- **Official documentation:** [List Nodes](https://doc.woztell.com/docs/reference/open-api-reference/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables` | body | `object` | no | Optional GraphQL variables object. Supported keys include treeIds, nodeIds, search, global, first, last, after, before, and sortBy. |
