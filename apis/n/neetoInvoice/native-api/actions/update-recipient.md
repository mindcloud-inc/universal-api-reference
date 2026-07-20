# Update Recipient with NeetoInvoice

Updates an existing recipient in NeetoInvoice.

## Endpoint

- **Method:** `PUT`
- **Path:** `/clients/{client_id}/recipients/{recipient_id}`
- **Base URL:** `https://{workspaceSubdomain}.neetoinvoice.com/api/external/v1`
- **Official documentation:** [Update Recipient](https://apidocs.neetoinvoice.com/api-reference/recipients/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | path | `string` | no | Parent client identifier. |
| `recipient_id` | path | `string` | no | Recipient identifier. |
