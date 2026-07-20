# Create Estimate with Zoho FSM

Creates a new estimate in Zoho FSM.

## Endpoint

- **Method:** `POST`
- **Path:** `/Estimates`
- **Base URL:** `{api_domain}/fsm/v1`
- **Official documentation:** [Create Estimate](https://www.zoho.com/fsm/developer/help/api/create-estimate.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data[0].Adjustment` | body | `number` | no |
| `data[0].Asset` | body | `string` | no |
| `data[0].Billing_Address.id` | body | `string` | no |
| `data[0].Company` | body | `string` | yes |
| `data[0].Contact` | body | `string` | yes |
| `data[0].Currency` | body | `string` | no |
| `data[0].Email` | body | `string` | no |
| `data[0].Exchange_Rate` | body | `number` | no |
| `data[0].Expiry_Date` | body | `date` | no |
| `data[0].Grand_Total` | body | `number` | no |
| `data[0].Phone` | body | `string` | no |
| `data[0].Service_Address.id` | body | `string` | no |
| `data[0].Service_Line_Items[].Amount` | body | `number` | no |
| `data[0].Service_Line_Items[].Contact` | body | `string` | no |
| `data[0].Service_Line_Items[].Description` | body | `string` | no |
| `data[0].Service_Line_Items[].Discount` | body | `number` | no |
| `data[0].Service_Line_Items[].Discount_Type` | body | `string` | no |
| `data[0].Service_Line_Items[].Line_Item_Amount` | body | `number` | no |
| `data[0].Service_Line_Items[].List_Price` | body | `number` | no |
| `data[0].Service_Line_Items[].Quantity` | body | `number` | no |
| `data[0].Service_Line_Items[].Sequence` | body | `number` | no |
| `data[0].Service_Line_Items[].Service` | body | `string` | yes |
| `data[0].Service_Line_Items[].Status` | body | `string` | no |
| `data[0].Service_Line_Items[].Tax.Tax_Exemption_Code` | body | `string` | no |
| `data[0].Service_Line_Items[].Tax.Tax_Exemption_Id` | body | `string` | no |
| `data[0].Service_Line_Items[].Tax.Tax_Id` | body | `string` | no |
| `data[0].Service_Line_Items[].Tax.Tax_Name` | body | `string` | no |
| `data[0].Service_Line_Items[].Tax.Tax_Percentage` | body | `number` | no |
| `data[0].Service_Line_Items[].Unit` | body | `string` | no |
| `data[0].Sub_Total` | body | `number` | no |
| `data[0].Summary` | body | `string` | yes |
| `data[0].Tax_Amount` | body | `number` | no |
| `data[0].Territory` | body | `string` | no |
