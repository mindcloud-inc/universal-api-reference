# Update a schedule by ID with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/campaign/schedule/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update a schedule by ID](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the schedule to update. |
| `body` | body | `object` | yes | Request body |
| `name` | body | `string` | yes | The name of the schedule. |
| `timeFrom` | body | `string` | yes | Start time for the schedule. |
| `timeTo` | body | `string` | yes | End time for the schedule. |
| `activeDays[]` | body | `array` | yes | List of active days for the schedule. |
| `timezone` | body | `string` | yes | Timezone of the schedule. |
