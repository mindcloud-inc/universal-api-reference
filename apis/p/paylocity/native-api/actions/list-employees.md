# List Employees with Paylocity

Retrieves the list of employees of a company

## Endpoint

- **Method:** `GET`
- **Path:** `coreHr/v1/companies/:companyId/employees`
- **Base URL:** `{connection}`
- **Official documentation:** [List Employees](https://developer.paylocity.com/integrations/reference/get_corehr-v1-companies-companyid-employees)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `string` | yes | Id of the company that is being accessed |
| `include` | query | `string` | no | — |
