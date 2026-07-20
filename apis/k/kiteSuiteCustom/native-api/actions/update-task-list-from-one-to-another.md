# Update task List from one to another with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/list/task/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update task List from one to another](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `id` | path | `string` | no | Task ID |
| `newListID` | body | `string` | yes | — |
| `position` | body | `string` | yes | — |
