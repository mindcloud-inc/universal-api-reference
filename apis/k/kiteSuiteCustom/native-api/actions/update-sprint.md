# Update Sprint with Kite Suite

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/sprint/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update Sprint](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `id` | path | `string` | no | Sprint Id |
| `sprintName` | body | `string` | yes | — |
| `startDate` | body | `string` | yes | — |
| `endDate` | body | `string` | yes | — |
| `duration` | body | `number` | yes | — |
| `sprintGoal` | body | `string` | yes | — |
