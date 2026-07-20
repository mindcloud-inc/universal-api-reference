# List Facility Addresses with Recreation.gov

Retrieves addresses for a facility from Recreation.gov.

## Endpoint

- **Method:** `GET`
- **Path:** `/facilities/{id}/facilityaddresses`
- **Base URL:** `https://ridb.recreation.gov/api/v1`
- **Official documentation:** [List Facility Addresses](https://ridb.recreation.gov/shared/swagger/ridb.yaml)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | — |
| `query` | query | `string` | no | Filter addresses by city, state, postal code, country code, or street fields. |
| `limit` | query | `number` | no | Maximum number of records to return. |
| `offset` | query | `number` | no | Number of records to skip before returning results. |
