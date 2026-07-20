# Update Order with VSCO Workspace

Updates an existing order in VSCO Workspace.

## Endpoint

- **Method:** `PUT`
- **Path:** `/order/:id`
- **Base URL:** `https://workspace.vsco.co/api/v2`
- **Official documentation:** [Update Order](https://workspace.vsco.co/api/#operation/updateResourceOrder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `jobId` | body | `string` | no | A lowercase [ULID](https://github.com/ulid/spec) entity identifier |
| `recipientId` | body | `string` | no | A ULID entity identifier that is nullable. |
| `dueDate` | body | `object` | no | — |
| `name` | body | `string` | no | — |
| `bookedOn` | body | `object` | no | — |
| `balance` | body | `object` | no | — |
| `lineItems[]` | body | `array<object>` | no | — |
| `taxGroupId` | body | `string` | no | A ULID entity identifier that is nullable. |
| `taxCombined` | body | `object` | no | — |
| `total` | body | `object` | no | — |
| `paymentTermsId` | body | `string` | no | A ULID entity identifier that is nullable. |
