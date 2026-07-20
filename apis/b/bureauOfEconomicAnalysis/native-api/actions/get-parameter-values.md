# Get Parameter Values with Bureau of Economic Analysis

Retrieves parameter values for a Bureau of Economic Analysis dataset.

## Endpoint

- **Method:** `GET`
- **Path:** `/data`
- **Base URL:** `https://apps.bea.gov/api`
- **Official documentation:** [Get Parameter Values](https://apps.bea.gov/api/_pdf/bea_web_service_api_user_guide.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `DataSetName` | query | `string` | yes | BEA dataset name, such as NIPA, Regional, or GDPbyIndustry. |
| `ParameterName` | query | `string` | yes | Parameter whose valid values should be returned. |
