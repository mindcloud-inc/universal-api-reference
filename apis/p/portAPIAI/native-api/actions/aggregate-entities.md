# Aggregate Entities with Port API AI

Retrieves aggregated entities from Port.

## Endpoint

- **Method:** `POST`
- **Path:** `/entities/aggregate`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Aggregate Entities](https://docs.port.io/api-reference/aggregate-entities)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `func` | body | `string` | yes | Aggregate function |
| `query` | body | `object` | yes | Aggregate query |
