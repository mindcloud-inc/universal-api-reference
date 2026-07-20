# Get Parameter List with Bureau of Economic Analysis

Retrieves parameters for a Bureau of Economic Analysis dataset.

## Endpoint

- **Method:** `GET`
- **Path:** `/data`
- **Base URL:** `https://apps.bea.gov/api`
- **Official documentation:** [Get Parameter List](https://apps.bea.gov/api/_pdf/bea_web_service_api_user_guide.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `DataSetName` | query | `string` | yes | BEA dataset name, such as NIPA, Regional, or GDPbyIndustry. |
