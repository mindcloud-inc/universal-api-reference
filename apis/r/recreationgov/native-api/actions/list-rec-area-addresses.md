# List Rec Area Addresses with Recreation.gov

Retrieves addresses for a recreation area from Recreation.gov.

## Endpoint

- **Method:** `GET`
- **Path:** `/recareas/{id}/recareaaddresses`
- **Base URL:** `https://ridb.recreation.gov/api/v1`
- **Official documentation:** [List Rec Area Addresses](https://ridb.recreation.gov/shared/swagger/ridb.yaml)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | — |
| `query` | query | `string` | no | Filter addresses by city, state, postal code, country code, or street fields. |
| `limit` | query | `number` | no | Maximum number of records to return. |
| `offset` | query | `number` | no | Number of records to skip before returning results. |
