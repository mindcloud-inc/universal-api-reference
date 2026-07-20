# change parent of a task by task Id with Kite Suite

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task/convert`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [change parent of a task by task Id](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `parentTask` | body | `string` | yes | — |
| `taskID` | body | `string` | yes | — |
| `isSubIssue` | body | `boolean` | yes | — |
