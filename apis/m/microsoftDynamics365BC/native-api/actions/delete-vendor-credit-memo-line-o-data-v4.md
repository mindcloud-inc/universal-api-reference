# Delete Vendor Credit Memo Line ODataV4 with Microsoft Dynamics 365 BC

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/ODataV4/Company(:company)/MindcloudPurchaseCreditMemoPurchLines(Document_Type=:Document_Type,Document_No=:Document_No,Line_No=:Line_No)`
- **Base URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/`
- **API:** REST

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | path | `list` | yes | Accepted values: `'Active260127'`, `'Esser%20Plumbing%20%26%20Heating'`. |
| `Document_Type` | path | `string` | no | — |
| `Document_No` | path | `string` | no | — |
| `Line_No` | path | `string` | no | — |
