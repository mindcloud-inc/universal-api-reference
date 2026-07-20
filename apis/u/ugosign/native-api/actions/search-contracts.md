# Search Contracts with Ugosign

Finds a contract in Ugosign by ID or text.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/contracts/search`
- **Base URL:** `https://app.ugosign.com/api`
- **Official documentation:** [Search Contracts](https://app.ugosign.com/api/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `field` | query | `string` | yes |
| `s` | query | `string` | yes |
