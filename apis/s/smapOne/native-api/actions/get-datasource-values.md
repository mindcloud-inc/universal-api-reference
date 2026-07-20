# Get datasource values with smapOne

Retrieves data source values from smapOne.

## Endpoint

- **Method:** `GET`
- **Path:** `/intern/DataSource/{dataSourceId}/Versions/{dataSourceVersion}/Definition/Values`
- **Base URL:** `https://platform.smapone.com/Backend`
- **Official documentation:** [Get datasource values](https://platform.smapone.com/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataSourceId` | path | `string` | yes | The datasource id. |
| `dataSourceVersion` | path | `string` | yes | The datasource version number, for example 1.0. |
