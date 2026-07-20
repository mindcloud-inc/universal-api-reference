# List Financial Documents for Matter with DecisionVault

Retrieves financial documents for a matter in DecisionVault.

## Endpoint

- **Method:** `GET`
- **Path:** `/matters/:matter_id/financial-documents`
- **Base URL:** `https://api.decisionvault.com/v1`
- **Official documentation:** [List Financial Documents for Matter](https://docs.decisionvault.com/get-financial-documents-for-matter-21745392e0.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `matter_id` | path | `string` | yes | The matter ID. |
| `uploaded_since` | query | `date` | no | Only include financial documents uploaded on or after this date. |
