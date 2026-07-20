# Delete Scheduled SMS with Nvoip

## Endpoint

- **Method:** `DELETE`
- **Path:** `/delete/sched/torpedo`
- **Base URL:** `https://api.nvoip.com.br/v2`
- **Official documentation:** [Delete Scheduled SMS](https://github.com/Nvoip/nvoip-integrationAPI/blob/main/index.js)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `schedkey` | query | `string` | yes | Identifier of the scheduled SMS to delete. |
