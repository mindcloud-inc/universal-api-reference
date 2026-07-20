# List Entity Invoices with Syntage

Retrieves invoices for an entity in Syntage.

## Endpoint

- **Method:** `GET`
- **Path:** `/entities/:entityId/invoices`
- **Base URL:** `https://api.sandbox.syntage.com`
- **Official documentation:** [List Entity Invoices](https://docs.syntage.com/api-reference/ds-mx-sat-invoices/list-all-taxpayers-invoices.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityId` | path | `string` | yes | The Syntage entity identifier. |
