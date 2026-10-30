# Mark Dispatch as Received with GoCanvas

## Endpoint

- **Method:** `PATCH`
- **Path:** `/dispatches/:dispatchId`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Mark Dispatch as Received](https://api.gocanvas.com/api/v3/docs#mark-a-dispatch-as-received)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dispatchId` | path | `number` | yes | Identifier of the assigned dispatch to acknowledge. |
