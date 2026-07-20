# Perform Work Order Transition with Zoho FSM

Performs a work order blueprint transition in Zoho FSM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/Work_Orders/:recordId/actions/blueprint`
- **Base URL:** `{api_domain}/fsm/v1`
- **Official documentation:** [Perform Work Order Transition](https://www.zoho.com/fsm/developer/help/api/perform-work-order-transition.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blueprint[].transition_id` | body | `string` | no | — |
| `recordId` | path | `string` | yes | The Zoho FSM record ID. |
