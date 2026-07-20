# List Entity Tax Compliance Checks with Syntage

Retrieves tax compliance checks for an entity in Syntage.

## Endpoint

- **Method:** `GET`
- **Path:** `/entities/:entityId/tax-compliance-checks`
- **Base URL:** `https://api.sandbox.syntage.com`
- **Official documentation:** [List Entity Tax Compliance Checks](https://docs.syntage.com/api-reference/ds-mx-sat-tax-compliance-checks/list-all-taxpayers-tax-compliance-checks.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityId` | path | `string` | yes | The Syntage entity identifier. |
