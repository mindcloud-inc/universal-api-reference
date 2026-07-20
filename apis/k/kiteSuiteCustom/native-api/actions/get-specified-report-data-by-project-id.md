# Get specified report data by projectId with Kite Suite

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/report/project/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Get specified report data by projectId](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Project ID |
| `type` | query | `string` | yes | Report type |
| `fieldName` | query | `string` | no | For Report type time-since-task |
| `maxData` | query | `string` | no | For Report type recently-created |
| `source` | query | `string` | no | For Report type recently-created |
