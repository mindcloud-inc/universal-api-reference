# Update Client Status with NeetoInvoice

Updates a client status in NeetoInvoice.

## Endpoint

- **Method:** `POST`
- **Path:** `/clients/update_status`
- **Base URL:** `https://{workspaceSubdomain}.neetoinvoice.com/api/external/v1`
- **Official documentation:** [Update Client Status](https://apidocs.neetoinvoice.com/api-reference/clients/update-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | body | `string` | no | Client identifier whose status will be updated. |
| `status` | body | `string` | no | New client status. |
