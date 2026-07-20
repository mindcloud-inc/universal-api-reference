# Update Day Note V2 with RotaCloud

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/dayNotes/:id`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [Update Day Note V2](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Day note ID. |
| `startDate` | body | `string` | yes | Day note start date in YYYY-MM-DD format. |
| `endDate` | body | `string` | yes | Day note end date in YYYY-MM-DD format. |
| `locations[]` | body | `array<number>` | yes | Location IDs affected by the day note. |
| `title` | body | `string` | yes | Day note title. |
| `message` | body | `string` | yes | Day note body text. |
| `visibleToEmployees` | body | `boolean` | yes | Whether employees can see the day note. |
