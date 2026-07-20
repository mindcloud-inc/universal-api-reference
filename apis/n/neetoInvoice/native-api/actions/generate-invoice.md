# Generate Invoice with NeetoInvoice

Generates an invoice for a client in NeetoInvoice.

## Endpoint

- **Method:** `POST`
- **Path:** `/clients/{client_id}/invoices`
- **Base URL:** `https://{workspaceSubdomain}.neetoinvoice.com/api/external/v1`
- **Official documentation:** [Generate Invoice](https://apidocs.neetoinvoice.com/api-reference/invoices/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | path | `string` | no | Client identifier. |
