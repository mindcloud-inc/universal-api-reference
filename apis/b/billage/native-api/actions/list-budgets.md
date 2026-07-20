# List Budgets with Billage

Retrieves budget records from Billage by code or date.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/budgets`
- **Base URL:** `https://app.getbillage.com/api`
- **Official documentation:** [List Budgets](https://app.getbillage.com/api/documentation.html#/Budgets/budgetsByParameters)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Search budgets |
| `colour` | query | `string` | no | Colour name |
