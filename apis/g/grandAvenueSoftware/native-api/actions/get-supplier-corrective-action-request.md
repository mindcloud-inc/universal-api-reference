# Get Supplier Corrective Action Request with Grand Avenue Software

Retrieves a supplier corrective action request from Grand Avenue Software by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/SupplierCorrectiveActionRequests/:id`
- **Base URL:** `{baseUrl}`
- **API:** REST

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$select` | query | `list<string>` | no | Send multiple values as a string. |
| `$expand` | query | `list<string>` | no | Send multiple values as a string. |
| `id` | path | `string` | yes | — |
