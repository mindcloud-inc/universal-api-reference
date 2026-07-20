# Create Order for Job with VSCO Workspace

Creates a new order for a job in VSCO Workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/job/:jobId/order`
- **Base URL:** `https://workspace.vsco.co/api/v2`
- **Official documentation:** [Create Order for Job](https://workspace.vsco.co/api/#operation/createResourceJobOrder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | — |
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
