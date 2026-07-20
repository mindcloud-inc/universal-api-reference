# List Rec Area Events with Recreation.gov

Retrieves events for a recreation area from Recreation.gov.

## Endpoint

- **Method:** `GET`
- **Path:** `/recareas/{id}/events`
- **Base URL:** `https://ridb.recreation.gov/api/v1`
- **Official documentation:** [List Rec Area Events](https://ridb.recreation.gov/shared/swagger/ridb.yaml)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | — |
| `query` | query | `string` | no | Filter events by name, dates, descriptions, age group, accessibility, fee, scope, or type. |
| `limit` | query | `number` | no | Maximum number of records to return. |
| `offset` | query | `number` | no | Number of records to skip before returning results. |
