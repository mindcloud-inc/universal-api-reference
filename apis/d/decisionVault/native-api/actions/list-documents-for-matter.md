# List Documents for Matter with DecisionVault

Retrieves documents for a matter in DecisionVault.

## Endpoint

- **Method:** `GET`
- **Path:** `/matters/:matter_id/documents`
- **Base URL:** `https://api.decisionvault.com/v1`
- **Official documentation:** [List Documents for Matter](https://docs.decisionvault.com/get-documents-for-matter-21745356e0.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `matter_id` | path | `string` | yes | The matter ID. |
| `uploaded_since` | query | `date` | no | Only include documents uploaded on or after this date. |
