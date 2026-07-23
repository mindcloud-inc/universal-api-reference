# Search For Expenditures with Rillion Prime

## Endpoint

- **Method:** `GET`
- **Path:** `/budget/search/role/:role`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Search For Expenditures](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Invoice%20-%20v1.0)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `role` | path | `string` | yes | Path value for Role. |
| `searchTerm` | query | `string` | no | Optional query value for SearchTerm. |
