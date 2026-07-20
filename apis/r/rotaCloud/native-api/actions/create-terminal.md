# Create Terminal with RotaCloud

Creates a terminal in RotaCloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/terminals`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [Create Terminal](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Terminal name. |
| `timezone` | body | `number` | yes | Timezone ID. |
