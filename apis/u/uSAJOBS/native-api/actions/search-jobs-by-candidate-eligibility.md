# Search Jobs By Candidate Eligibility with USAJOBS

Finds jobs in USAJOBS by candidate eligibility.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/Search`
- **Base URL:** `https://data.usajobs.gov`
- **Official documentation:** [Search Jobs By Candidate Eligibility](https://developer.usajobs.gov/api-reference/get-api-search)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `WhoMayApply` | query | `string` | no | Candidate designation such as Public. |
