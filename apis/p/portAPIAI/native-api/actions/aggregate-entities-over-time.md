# Aggregate Entities Over Time with Port API AI

Retrieves entity aggregates over time from Port.

## Endpoint

- **Method:** `POST`
- **Path:** `/entities/aggregate-over-time`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Aggregate Entities Over Time](https://docs.port.io/api-reference/aggregate-entities-over-time)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `aggregationType` | body | `string` | yes | Aggregation mode discriminator for Port aggregate-over-time |
| `blueprint` | body | `string` | yes | Blueprint identifier |
| `func` | body | `string` | yes | Aggregation function |
| `properties[]` | body | `array<string>` | yes | Property paths to aggregate |
| `measureTimeBy` | body | `string` | yes | Time property path used for bucketing |
| `query` | body | `object` | yes | Port search query object |
| `timeInterval` | body | `string` | yes | Bucket interval |
| `timeRange` | body | `object` | yes | Preset time range object |
