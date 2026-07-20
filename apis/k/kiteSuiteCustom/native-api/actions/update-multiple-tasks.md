# update multiple tasks with Kite Suite

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task/multiple`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [update multiple tasks](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `projectID` | body | `string` | yes | — |
| `tasks[]` | body | `array` | yes | — |
| `assigneeId` | body | `string` | yes | — |
| `epic` | body | `string` | yes | — |
| `sprint` | body | `string` | yes | — |
| `dueDate` | body | `string` | yes | — |
