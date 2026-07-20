# List Companies with Recommand

Retrieves company records from the Recommand API.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/companies`
- **Base URL:** `https://app.recommand.eu`
- **Official documentation:** [List Companies](https://recommand.eu/en/reference/companies/list-companies)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `enterpriseNumber` | query | `string` | no | enterpriseNumber parameter. |
| `vatNumber` | query | `string` | no | vatNumber parameter. |
