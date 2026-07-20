# Clock In User with RotaCloud

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/users_clocked_in/:id`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [Clock In User](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | User ID to clock in. |
| `method` | body | `string` | yes | Clock-in method. |
