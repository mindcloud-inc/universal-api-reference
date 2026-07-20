# Clock Out User with RotaCloud

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/users_clocked_in/:id`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [Clock Out User](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action` | body | `string` | yes | Clock-out action value. |
| `id` | path | `number` | yes | User ID to clock out. |
| `method` | body | `string` | yes | Clock-out method. |
