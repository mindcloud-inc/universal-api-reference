# Get Scoped Time Series with International Monetary Fund

Retrieves IMF time series by country, region, or group.

## Endpoint

- **Method:** `GET`
- **Path:** `/:indicatorId/:selectionPath`
- **Base URL:** `https://www.imf.org/external/datamapper/api/v1`
- **Official documentation:** [Get Scoped Time Series](https://www.imf.org/external/datamapper/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `indicatorId` | path | `string` | yes | IMF indicator identifier, such as NGDP_RPCH for real GDP growth. |
| `selectionPath` | path | `string` | yes | Slash-delimited country, region, or analytical-group IDs, such as USA/CHN or EUQ. |
| `periods` | query | `string` | no | Optional comma-separated list of years to restrict the series, for example 2019,2020. |
