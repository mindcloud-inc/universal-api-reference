# Create Action with 4HSE

Creates a new action in 4HSE.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/action/create`
- **Base URL:** `https://service.4hse.com`
- **Official documentation:** [Create Action](https://docs.4hse.com/en/api/action/#operation-createAction-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action_type` | body | `string` | yes | Type of preventive action. Accepted values: `0`, `1`, `2`, `3`, `4`. |
| `code` | body | `string` | no | Identifier code for the action. |
| `name` | body | `string` | yes | Descriptive name of the action. |
| `description` | body | `string` | no | Optional detailed description. |
| `validity_unit` | body | `string` | no | Unit for the certificate validity period. Accepted values: `0`, `1`, `2`. |
| `validity` | body | `number` | no | Number of validity units. |
| `expire_interval` | body | `number` | no | Days before expiration to trigger EXPIRING status. |
| `subtenant_id` | body | `string` | yes | The office where this action is defined. |
| `tenant_id` | body | `string` | yes | The project this action belongs to. |
