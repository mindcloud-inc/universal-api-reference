# Get Invoice Account Coding History with Rillion Prime

## Endpoint

- **Method:** `GET`
- **Path:** `/invoice/:invoiceId/invoiceAccountCodingLog/role/:role`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Get Invoice Account Coding History](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoiceId` | path | `number` | yes | Path value for InvoiceId. |
| `role` | path | `string` | yes | Path value for Role. |
