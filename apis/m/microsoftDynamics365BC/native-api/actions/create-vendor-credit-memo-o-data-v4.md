# Create Vendor Credit Memo ODataV4 with Microsoft Dynamics 365 BC

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/ODataV4/Company(:company)/MincloudPurchaseInvoice`
- **Base URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/`
- **API:** REST

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | path | `list` | yes | Accepted values: `'Active260127'`, `'Esser%20Plumbing%20%26%20Heating'`. |
| `Document_Type` | body | `string` | no | — |
| `Buy_from_Vendor_No` | body | `string` | no | — |
| `Buy_from_Vendor_Name` | body | `string` | no | — |
| `Pay_to_Name` | body | `string` | no | — |
| `Vendor_Invoice_No` | body | `string` | no | — |
| `Document_Date` | body | `string` | no | — |
| `Posting_Date` | body | `string` | no | — |
| `Shortcut_Dimension_1_Code` | body | `string` | no | — |
| `Shortcut_Dimension_2_Code` | body | `string` | no | — |
| `Location_Code` | body | `string` | no | — |
| `DocAmount` | body | `string` | no | — |
| `Vendor_Cr_Memo_No` | body | `string` | no | — |
| `Applies_to_Doc_Type` | body | `string` | no | — |
| `Applies_to_Doc_No` | body | `string` | no | — |
