# Search Clients By Title with Outlign

Finds clients in Outlign by title.

## Endpoint

- **Method:** `GET`
- **Path:** `/clients`
- **Base URL:** `https://go.outlign.co/api/v1`
- **Official documentation:** [Search Clients By Title](https://go.outlign.co/api/docs/clients)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | query | `string` | yes | Filter clients by title using partial match |
| `per_page` | query | `number` | no | Number of results per page (max 1000) |
