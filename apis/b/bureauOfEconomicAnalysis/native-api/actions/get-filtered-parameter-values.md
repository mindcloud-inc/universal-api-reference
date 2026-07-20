# Get Filtered Parameter Values with Bureau of Economic Analysis

Retrieves filtered parameter values for a Bureau of Economic Analysis dataset.

## Endpoint

- **Method:** `GET`
- **Path:** `/data`
- **Base URL:** `https://apps.bea.gov/api`
- **Official documentation:** [Get Filtered Parameter Values](https://apps.bea.gov/api/_pdf/bea_web_service_api_user_guide.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `DataSetName` | query | `string` | yes | BEA dataset name. Filtered values are not implemented for every dataset. |
| `TargetParameter` | query | `string` | yes | The parameter for which valid values should be returned. |
| `TableName` | query | `string` | no | Optional table name used to filter target values when supported. |
| `GeoFIPS` | query | `string` | no | Optional state, county, or MSA code for Regional filters. |
| `Year` | query | `string` | no | Optional year or comma-separated year list. |
