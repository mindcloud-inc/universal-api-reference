# Perform Request Transition with Zoho FSM

Performs a request blueprint transition in Zoho FSM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/Requests/:recordId/actions/blueprint`
- **Base URL:** `{api_domain}/fsm/v1`
- **Official documentation:** [Perform Request Transition](https://www.zoho.com/fsm/developer/help/api/perform-request-transition.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blueprint[].transition_id` | body | `string` | yes | — |
| `recordId` | path | `string` | yes | The Zoho FSM record ID. |
