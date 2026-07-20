# Create Credit Memo Itens ODataV4 with Microsoft Dynamics 365 BC

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/ODataV4/Company(:company)/MindcloudCreditMemoSalesLines`
- **Base URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/`
- **API:** REST

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `company` | path | `list` | no |
| `Type` | body | `string` | no |
| `No` | body | `string` | no |
| `Item_Reference_No` | body | `string` | no |
| `Description` | body | `string` | no |
| `Quantity` | body | `number` | no |
| `Unit_Price` | body | `number` | no |
| `Tax_Area_Code` | body | `string` | no |
| `Line_Amount` | body | `number` | no |
| `Allow_Invoice_Disc` | body | `boolean` | no |
| `Shortcut_Dimension_1_Code` | body | `string` | no |
| `Work_Type_Code` | body | `string` | no |
| `Document_No` | body | `string` | no |
| `Description_2` | body | `string` | no |
