# Search Companies with Perigon

Finds companies in Perigon by name, symbol, or domain.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/companies/all`
- **Base URL:** `https://api.perigon.io/v1`
- **Official documentation:** [Search Companies](https://docs.perigon.io/docs/company-data)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | — |
| `id` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `symbol` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `domain` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `country` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `exchange` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `numEmployeesFrom` | query | `number` | no | — |
| `numEmployeesTo` | query | `number` | no | — |
| `ipoFrom` | query | `date` | no | — |
| `ipoTo` | query | `date` | no | — |
| `name` | query | `string` | no | — |
| `industry` | query | `string` | no | — |
| `sector` | query | `string` | no | — |
| `size` | query | `number` | no | — |
| `page` | query | `number` | no | — |
