# Create Action Session with 4HSE

Creates a new action session in 4HSE.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/action-session/create`
- **Base URL:** `https://service.4hse.com`
- **Official documentation:** [Create Action Session](https://docs.4hse.com/en/api/actionsession/#operation-createActionSession-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action_id` | body | `string` | yes | The action this session belongs to. |
| `validity_unit` | body | `string` | no | Validity unit specific to this session. Accepted values: `0`, `1`, `2`. |
| `validity` | body | `number` | no | Number of validity units specific to this session. |
| `data` | body | `object` | no | Structured session data by action type. |
| `subtenant_id` | body | `string` | yes | The office of this session. |
| `tenant_id` | body | `string` | yes | The project of this session. |
