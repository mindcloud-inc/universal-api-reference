# List Invoices with Jobber

## Endpoint

- **Method:** `POST`
- **Path:** `graphql`
- **Base URL:** `https://api.getjobber.com/api`
- **Official documentation:** [List Invoices](https://developer.getjobber.com/docs/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `columns` | body | `string` | no | Select the Jobber invoice fields to return. |
| `createdAfter` | body | `date` | no | Only return invoices created after this timestamp (ISO 8601). Maps to filter.createdAt.after on the Jobber invoices query. |
| `createdBefore` | body | `date` | no | Only return invoices created before this timestamp (ISO 8601). Maps to filter.createdAt.before on the Jobber invoices query. |
| `clientId` | body | `string` | no | Only return invoices for the specified Jobber client id. |
| `invoiceNumber` | body | `string` | no | Only return the invoice matching the specified invoice number. |
| `status` | body | `string` | no | Only return invoices with the specified Jobber invoice status. |
| `excludeOrigin` | body | `string` | no | Exclude invoices with one or more of the specified Jobber invoice origins. Send multiple values as a array. |
| `updatedAfter` | body | `date` | no | Only return invoices updated after this timestamp (ISO 8601). Maps to filter.updatedAt.after on the Jobber invoices query. |
| `updatedBefore` | body | `date` | no | Only return invoices updated before this timestamp (ISO 8601). Maps to filter.updatedAt.before on the Jobber invoices query. |
