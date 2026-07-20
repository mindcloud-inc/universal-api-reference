# Datasets PutTable with Microsoft Power BI

## Endpoint

- **Method:** `PUT`
- **Path:** `datasets/[:datasetId]/tables/[:tableName]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Datasets PutTable](https://learn.microsoft.com/en-us/rest/api/power-bi/push-datasets/datasets-put-table)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetId` | path | `string` | yes | The dataset ID |
| `tableName` | path | `string` | yes | The table name |
| `columns[]` | body | `array<object>` | yes | The column schema for this table |
| `name` | body | `string` | yes | The table name |
| `description` | body | `string` | no | The table description |
| `isHidden` | body | `boolean` | no | Optional. Whether this dataset table is hidden. |
| `measures[]` | body | `array<object>` | no | The measures within this table |
| `rows[]` | body | `array<object>` | no | The data rows within this table |
| `source[]` | body | `array<object>` | no | The table source |
