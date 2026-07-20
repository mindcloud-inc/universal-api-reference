# List Metrics with Reportei

Retrieves metrics from Reportei.

## Endpoint

- **Method:** `GET`
- **Path:** `/metrics`
- **Base URL:** `https://app.reportei.com/api/v2`
- **Official documentation:** [List Metrics](https://developers.reportei.com#metricas-endpoint-0)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `integration_slug` | query | `string` | yes | Slug da integração. |
