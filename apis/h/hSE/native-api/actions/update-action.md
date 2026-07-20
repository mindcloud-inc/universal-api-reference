# Update Action with 4HSE

Updates an existing action in 4HSE.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/action/update/:id`
- **Base URL:** `https://service.4hse.com`
- **Official documentation:** [Update Action](https://docs.4hse.com/en/api/action/#operation-updateAction-put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The action_id to update. |
| `name` | body | `string` | yes | Descriptive name of the action. |
| `validity` | body | `number` | no | Number of validity units. |
