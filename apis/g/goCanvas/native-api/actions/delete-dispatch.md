# Delete Dispatch with GoCanvas

## Endpoint

- **Method:** `DELETE`
- **Path:** `/dispatches/:dispatchId`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Delete Dispatch](https://api.gocanvas.com/api/v3/docs#delete-a-dispatch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dispatchId` | path | `number` | yes | Identifier of the dispatch to delete. |
| `hard_delete` | query | `boolean` | no | When true, permanently deletes the dispatch. Omit or use false to soft-delete it. |
