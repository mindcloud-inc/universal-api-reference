# List Rec Area Activities with Recreation.gov

Retrieves activities for a recreation area from Recreation.gov.

## Endpoint

- **Method:** `GET`
- **Path:** `/recareas/{id}/activities`
- **Base URL:** `https://ridb.recreation.gov/api/v1`
- **Official documentation:** [List Rec Area Activities](https://ridb.recreation.gov/shared/swagger/ridb.yaml)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | — |
| `query` | query | `string` | no | Filter activities by name. |
| `limit` | query | `number` | no | Maximum number of records to return. |
| `offset` | query | `number` | no | Number of records to skip before returning results. |
