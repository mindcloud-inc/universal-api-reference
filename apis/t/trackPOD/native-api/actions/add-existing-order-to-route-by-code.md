# Add Existing Order To Route By Code with Track-POD

Updates a Track-POD route by adding an existing order by number.

## Endpoint

- **Method:** `PUT`
- **Path:** `/Route/Code/:code/Order/Number/:number`
- **Base URL:** `https://api.track-pod.com`
- **Official documentation:** [Add Existing Order To Route By Code](https://api.track-pod.com/index.html#/Route/MoveOrderToRouteByCodeByNumber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Route code |
| `number` | path | `string` | yes | Order number |
| `allowTransfer` | query | `boolean` | no | Allow transfer from another route |
| `allowReschedule` | query | `boolean` | no | Allow reschedule from another route |
