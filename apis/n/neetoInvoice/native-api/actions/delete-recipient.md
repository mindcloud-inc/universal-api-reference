# Delete Recipient with NeetoInvoice

Deletes an existing recipient from NeetoInvoice.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/clients/{client_id}/recipients/{recipient_id}`
- **Base URL:** `https://{workspaceSubdomain}.neetoinvoice.com/api/external/v1`
- **Official documentation:** [Delete Recipient](https://apidocs.neetoinvoice.com/api-reference/recipients/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | path | `string` | no | Parent client identifier. |
| `recipient_id` | path | `string` | no | Recipient identifier. |
