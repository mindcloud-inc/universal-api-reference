# Update Day Note with RotaCloud

Updates a day note in RotaCloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/day_notes/:id`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [Update Day Note](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Day note ID. |
| `start_date` | body | `string` | yes | Day note start date in YYYY-MM-DD format. |
| `end_date` | body | `string` | yes | Day note end date in YYYY-MM-DD format. |
| `locations[]` | body | `array<number>` | yes | Location IDs affected by the day note. |
| `title` | body | `string` | yes | Day note title. |
| `message` | body | `string` | yes | Day note body text. |
| `visible_employees` | body | `boolean` | yes | Whether employees can see the day note. |
