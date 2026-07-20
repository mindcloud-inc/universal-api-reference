# Apply Payment to Order with VSCO Workspace

Applies a payment to an order in VSCO Workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/payment/:id/apply`
- **Base URL:** `https://workspace.vsco.co/api/v2`
- **Official documentation:** [Apply Payment to Order](https://workspace.vsco.co/api/#operation/createResourceApplyPaymentToOrder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `orderId` | body | `string` | yes | A lowercase [ULID](https://github.com/ulid/spec) entity identifier |
| `amount` | body | `number` | yes | — |
