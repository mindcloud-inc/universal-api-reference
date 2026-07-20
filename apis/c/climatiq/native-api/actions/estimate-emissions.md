# Estimate Emissions with Climatiq

Estimates emissions in Climatiq from activity data.

## Endpoint

- **Method:** `POST`
- **Path:** `/data/v1/estimate`
- **Base URL:** `https://api.climatiq.io`
- **Official documentation:** [Estimate Emissions](https://www.climatiq.io/docs/api-reference/estimate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emission_factor` | body | `object` | yes | Emission factor selector object, such as activity_id and data_version. |
| `parameters` | body | `object` | yes | Activity data parameters object matching the selected factor unit type. |
