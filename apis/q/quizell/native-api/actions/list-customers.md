# List Customers with Quizell

Finds customers in Quizell with search and pagination.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers/list`
- **Base URL:** `https://api.quizell.com/api/v1`
- **Official documentation:** [List Customers](https://docs.quizell.com/customer-apis#list-customers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search term to filter customers by name, email, etc. |
