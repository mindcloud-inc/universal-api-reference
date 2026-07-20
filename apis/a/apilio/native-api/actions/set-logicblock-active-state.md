# Set Logicblock Active State with Apilio

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/logicblocks/{{uuid}}`
- **Base URL:** `https://api.apilio.com`
- **Official documentation:** [Set Logicblock Active State](https://documenter.getpostman.com/view/13480928/TzCHAVD2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `logicblock.active` | body | `boolean` | yes | Whether the logicblock should be active. |
| `uuid` | path | `string` | yes | The UUID of the logicblock to update. |
