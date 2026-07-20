# Scale Process with Cloud 66

Scales a process in your Cloud 66 account.

## Endpoint

- **Method:** `POST`
- **Path:** `/stacks/:stack_id/processes/:id/scale`
- **Base URL:** `https://app.cloud66.com/api/3`
- **Official documentation:** [Scale Process](https://developers.cloud66.com/v3/endpoints/processes/#scale-process)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stack_id` | path | `string` | yes | The stack UID |
| `id` | path | `string` | yes | The process ID |
