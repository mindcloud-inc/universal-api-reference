# Update Action Session with 4HSE

Updates an existing action session in 4HSE.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/action-session/update/:id`
- **Base URL:** `https://service.4hse.com`
- **Official documentation:** [Update Action Session](https://docs.4hse.com/en/api/actionsession/#operation-updateActionSession-put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The action session to update. |
| `action_id` | body | `string` | yes | The action this session belongs to. |
| `validity_unit` | body | `string` | no | Validity unit specific to this session. Accepted values: `0`, `1`, `2`. |
| `validity` | body | `number` | no | Number of validity units specific to this session. |
| `data` | body | `object` | no | Structured session data by action type. |
| `subtenant_id` | body | `string` | yes | The office of this session. |
| `tenant_id` | body | `string` | yes | The project of this session. |
