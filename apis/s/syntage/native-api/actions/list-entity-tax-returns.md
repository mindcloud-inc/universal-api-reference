# List Entity Tax Returns with Syntage

Retrieves tax returns for an entity in Syntage.

## Endpoint

- **Method:** `GET`
- **Path:** `/entities/:entityId/tax-returns`
- **Base URL:** `https://api.sandbox.syntage.com`
- **Official documentation:** [List Entity Tax Returns](https://docs.syntage.com/api-reference/ds-mx-sat-tax-returns/list-all-taxpayers-tax-returns.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityId` | path | `string` | yes | The Syntage entity identifier. |
