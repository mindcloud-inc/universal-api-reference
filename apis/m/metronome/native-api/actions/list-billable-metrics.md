# List Billable Metrics with Metronome

Retrieves billable metrics from Metronome.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/billable-metrics`
- **Base URL:** `https://api.metronome.com`
- **Official documentation:** [List Billable Metrics](https://docs.metronome.com/api-reference/billable-metrics/list-all-billable-metrics)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_archived` | query | `boolean` | no | Include archived billable metrics in the response. |
