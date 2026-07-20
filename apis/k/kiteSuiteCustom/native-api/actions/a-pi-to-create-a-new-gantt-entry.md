# API to create a new Gantt entry with Kite Suite

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/gantt`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [API to create a new Gantt entry](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `title` | body | `string` | yes | — |
| `projectID` | body | `string` | yes | — |
| `createdBy` | body | `string` | yes | — |
| `isEnable` | body | `boolean` | yes | — |
| `view` | body | `string` | yes | — |
