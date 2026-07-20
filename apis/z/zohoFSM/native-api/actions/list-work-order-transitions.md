# List Work Order Transitions with Zoho FSM

Retrieves available work order transitions from Zoho FSM.

## Endpoint

- **Method:** `GET`
- **Path:** `/Work_Orders/:recordId/actions/blueprint/transitions`
- **Base URL:** `{api_domain}/fsm/v1`
- **Official documentation:** [List Work Order Transitions](https://www.zoho.com/fsm/developer/help/api/list-work-order-transitions.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recordId` | path | `string` | yes | The Zoho FSM record ID. |
