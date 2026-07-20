# Delete Route By Code with Track-POD

Deletes an existing route from Track-POD by code.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/Route/Code/:code`
- **Base URL:** `https://api.track-pod.com`
- **Official documentation:** [Delete Route By Code](https://api.track-pod.com/index.html#/Route/DeleteRouteByCode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Route code |
| `deleteOrders` | query | `boolean` | no | Delete route orders too |
