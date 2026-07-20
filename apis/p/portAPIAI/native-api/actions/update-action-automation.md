# Update Action Automation with Port API AI

Updates an action automation in Port.

## Endpoint

- **Method:** `PUT`
- **Path:** `/actions/:action_identifier`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Update Action Automation](https://docs.port.io/api-reference/change-an-action-automation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action_identifier` | path | `string` | yes | The action identifier. |
| `identifier` | body | `string` | yes | The action identifier. |
| `invocationMethod` | body | `object` | yes | The invocation method object. |
| `trigger` | body | `object` | yes | The action trigger object. |
