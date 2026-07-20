# List Clients By Company with Outlign

Retrieves client records from Outlign by company.

## Endpoint

- **Method:** `GET`
- **Path:** `/clients`
- **Base URL:** `https://go.outlign.co/api/v1`
- **Official documentation:** [List Clients By Company](https://go.outlign.co/api/docs/clients)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | query | `number` | yes | Filter clients by company ID |
| `per_page` | query | `number` | no | Number of results per page (max 1000) |
