# Start User Break with RotaCloud

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/users_clocked_in/:id`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [Start User Break](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action` | body | `string` | yes | Break action name. |
| `id` | path | `number` | yes | User ID on break. |
| `method` | body | `string` | yes | Break start method. |
