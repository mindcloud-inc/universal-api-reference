# sync data by project Id with Kite Suite

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/report/timesheet`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [sync data by project Id](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `userID` | body | `string` | yes | — |
| `projectID` | body | `string` | yes | — |
| `startDate` | body | `string` | yes | — |
| `endDate` | body | `string` | yes | — |
