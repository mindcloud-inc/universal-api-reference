# List Invoices with Rillion Prime

## Endpoint

- **Method:** `GET`
- **Path:** `/invoice`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List Invoices](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Environment` | query | `string` | yes | Optional query value for Environment. |
| `User` | query | `string` | yes | Optional query value for User. |
| `Role` | query | `string` | no | Optional query value for Role. |
| `ForProcessing` | query | `number` | no | Optional query value for ForProcessing. |
