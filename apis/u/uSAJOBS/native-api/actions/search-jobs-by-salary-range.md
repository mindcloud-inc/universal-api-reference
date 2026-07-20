# Search Jobs By Salary Range with USAJOBS

Finds jobs in USAJOBS by salary range.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/Search`
- **Base URL:** `https://data.usajobs.gov`
- **Official documentation:** [Search Jobs By Salary Range](https://developer.usajobs.gov/api-reference/get-api-search)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `RemunerationMaximumAmount` | query | `string` | no | Maximum salary amount used for salary bucket matching. |
| `RemunerationMinimumAmount` | query | `string` | no | Minimum salary amount used for salary bucket matching. |
