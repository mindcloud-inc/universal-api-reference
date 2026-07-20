# Create Card On List with Placker

## Endpoint

- **Method:** `POST`
- **Path:** `/list/:list/card`
- **Base URL:** `https://api.placker.com`
- **Official documentation:** [Create Card On List](https://placker.com/docs/api/paths/list.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list` | path | `number` | yes | List ID. |
| `title` | body | `string` | yes | Card title. |
| `description` | body | `string` | no | Card description. |
| `status` | body | `string` | no | Card status. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`. |
| `startDates.planned` | body | `date` | no | Planned start date. |
| `startDates.actual` | body | `date` | no | Actual start date. |
| `endDates.planned` | body | `date` | no | Planned end date. |
| `endDates.actual` | body | `date` | no | Actual end date. |
| `order` | body | `number` | no | Card order within the list. |
