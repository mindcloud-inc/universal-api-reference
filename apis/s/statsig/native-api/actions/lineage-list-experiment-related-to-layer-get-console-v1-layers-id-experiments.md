# Lineage: List Experiment related to Layer with Statsig

Retrieves experiments related to a Statsig layer.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/layers/{id}/experiments`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Lineage: List Experiment related to Layer](https://docs.statsig.com/api-reference/layers/lineage-list-experiment-related-to-layer)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `limit` | query | `number` | no | Results per page |
| `page` | query | `number` | no | Page number |
