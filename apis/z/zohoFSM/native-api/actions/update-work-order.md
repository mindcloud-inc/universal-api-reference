# Update Work Order with Zoho FSM

Updates an existing work order in Zoho FSM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/Work_Orders/:recordId`
- **Base URL:** `{api_domain}/fsm/v1`
- **Official documentation:** [Update Work Order](https://www.zoho.com/fsm/developer/help/api/edit-work-order.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[0].Service_Line_Items[0].$fsm_delete` | body | `boolean` | no | — |
| `data[0].Service_Line_Items[0].id` | body | `string` | no | — |
| `data[0].Service_Line_Items[0].Part_Line_Items[0].$fsm_delete` | body | `boolean` | no | — |
| `data[0].Service_Line_Items[0].Part_Line_Items[0].id` | body | `string` | no | — |
| `data[0].Service_Line_Items[0].Quantity` | body | `number` | no | — |
| `data[0].Summary` | body | `string` | no | — |
| `recordId` | path | `string` | yes | The Zoho FSM record ID. |
