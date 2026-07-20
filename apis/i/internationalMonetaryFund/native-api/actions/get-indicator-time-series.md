# Get Indicator Time Series with International Monetary Fund

Retrieves IMF time series for a single indicator.

## Endpoint

- **Method:** `GET`
- **Path:** `/:indicatorId`
- **Base URL:** `https://www.imf.org/external/datamapper/api/v1`
- **Official documentation:** [Get Indicator Time Series](https://www.imf.org/external/datamapper/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `indicatorId` | path | `string` | yes | IMF indicator identifier, such as NGDP_RPCH for real GDP growth. |
| `periods` | query | `string` | no | Optional comma-separated list of years to restrict the series, for example 2019,2020. |
