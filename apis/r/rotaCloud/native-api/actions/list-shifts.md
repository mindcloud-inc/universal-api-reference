# List Shifts with RotaCloud

Lists shifts in RotaCloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/shifts`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [List Shifts](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | query | `number` | yes | Unix timestamp for the start of the shift window. |
| `end` | query | `number` | yes | Unix timestamp for the end of the shift window. |
