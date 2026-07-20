# Plant Trees with Digital Humani

Creates a tree-planting request in Digital Humani.

## Endpoint

- **Method:** `POST`
- **Path:** `/tree`
- **Base URL:** `https://api.digitalhumani.com`
- **Official documentation:** [Plant Trees](https://docs.digitalhumani.com/#apitree_plant)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | body | `string` | yes | The Digital Humani project ID where the trees should be planted. |
| `treeCount` | body | `number` | yes | The number of trees to plant. |
| `user` | body | `string` | yes | The end user associated with the tree-planting request. |
