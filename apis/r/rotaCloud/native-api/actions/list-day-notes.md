# List Day Notes with RotaCloud

Lists day notes in RotaCloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/day_notes`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [List Day Notes](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | query | `string` | yes | Start date for the day-note window in YYYY-MM-DD format. |
| `end` | query | `string` | yes | End date for the day-note window in YYYY-MM-DD format. |
