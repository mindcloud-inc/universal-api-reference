# Get Transition Rule with Qntrl

Retrieves a transition rule from Qntrl.

## Endpoint

- **Method:** `GET`
- **Path:** `/[:org_id]/transitionrule/[:transition_rule_id]`
- **Base URL:** `https://coreapi.qntrl.com/blueprint/api`
- **Official documentation:** [Get Transition Rule](https://core.qntrl.com/apidoc.html#getTransitionRule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | no | Qntrl organization ID. |
| `transition_rule_id` | path | `string` | no | Qntrl transition rule ID. |
