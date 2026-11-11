# Create Vendor Credit Memo Line ODataV4 with Microsoft Dynamics 365 BC

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/ODataV4/Company(:company)/MindcloudPurchaseCreditMemoPurchLines`
- **Base URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/`
- **API:** REST

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | path | `list` | yes | Accepted values: `'Active260127'`, `'Esser%20Plumbing%20%26%20Heating'`. |
| `Document_Type` | body | `string` | no | — |
| `Document_No` | body | `string` | no | — |
| `Type` | body | `string` | no | — |
| `No` | body | `string` | no | — |
| `Description` | body | `string` | no | — |
| `Quantity` | body | `string` | no | — |
| `Direct_Unit_Cost` | body | `string` | no | — |
| `Shortcut_Dimension_1_Code` | body | `string` | no | — |
| `Shortcut_Dimension_2_Code` | body | `string` | no | — |
| `Location_Code` | body | `string` | no | — |
