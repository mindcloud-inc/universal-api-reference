# Create Day Note V2 with RotaCloud

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/dayNotes`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [Create Day Note V2](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startDate` | body | `string` | yes | Day note start date in YYYY-MM-DD format. |
| `endDate` | body | `string` | yes | Day note end date in YYYY-MM-DD format. |
| `locations[]` | body | `array<number>` | yes | Location IDs affected by the day note. |
| `title` | body | `string` | yes | Day note title. |
| `message` | body | `string` | yes | Day note body text. |
| `visibleToEmployees` | body | `boolean` | yes | Whether employees can see the day note. |
