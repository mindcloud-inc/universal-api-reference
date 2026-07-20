# List Request Transitions with Zoho FSM

Retrieves available request transitions from Zoho FSM.

## Endpoint

- **Method:** `GET`
- **Path:** `/Requests/:recordId/actions/blueprint/transitions`
- **Base URL:** `{api_domain}/fsm/v1`
- **Official documentation:** [List Request Transitions](https://www.zoho.com/fsm/developer/help/api/list-request-transitions.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recordId` | path | `string` | yes | The Zoho FSM record ID. |
