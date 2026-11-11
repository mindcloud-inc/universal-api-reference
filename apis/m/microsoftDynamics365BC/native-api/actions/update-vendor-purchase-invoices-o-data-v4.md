# Update Vendor Purchase Invoices ODataV4 with Microsoft Dynamics 365 BC

## Endpoint

- **Method:** `PATCH`
- **Path:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/ODataV4/Company(:company)/MincloudPurchaseInvoice(No=:No,Document_Type=:Document_Type)`
- **Base URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/`
- **API:** REST

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | path | `list` | yes | Accepted values: `'Active260127'`, `'Esser%20Plumbing%20%26%20Heating'`. |
| `Vendor_Invoice_No` | body | `string` | no | — |
| `Document_Date` | body | `string` | no | — |
| `Posting_Date` | body | `string` | no | — |
| `Shortcut_Dimension_1_Code` | body | `string` | no | — |
| `Shortcut_Dimension_2_Code` | body | `string` | no | — |
| `Location_Code` | body | `string` | no | — |
| `No` | path | `string` | no | — |
| `Document_Type` | path | `string` | no | — |
