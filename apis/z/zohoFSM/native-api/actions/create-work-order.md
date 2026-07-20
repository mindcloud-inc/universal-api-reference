# Create Work Order with Zoho FSM

Creates a new work order in Zoho FSM.

## Endpoint

- **Method:** `POST`
- **Path:** `/Work_Orders`
- **Base URL:** `{api_domain}/fsm/v1`
- **Official documentation:** [Create Work Order](https://www.zoho.com/fsm/developer/help/api/create-work-order.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data[].$record_template` | body | `string` | no |
| `data[].Adjustment` | body | `string` | no |
| `data[].Asset` | body | `string` | no |
| `data[].Billing_Address.id` | body | `string` | no |
| `data[].Company` | body | `string` | no |
| `data[].Contact` | body | `string` | no |
| `data[].Currency` | body | `string` | no |
| `data[].Exchange_Rate` | body | `number` | no |
| `data[].Grand_Total` | body | `number` | no |
| `data[].Service_Address.id` | body | `string` | no |
| `data[].Service_Line_Items[].Amount` | body | `number` | no |
| `data[].Service_Line_Items[].Contact` | body | `string` | no |
| `data[].Service_Line_Items[].Description` | body | `string` | no |
| `data[].Service_Line_Items[].Discount` | body | `string` | no |
| `data[].Service_Line_Items[].Discount_Type` | body | `string` | no |
| `data[].Service_Line_Items[].Line_Item_Amount` | body | `number` | no |
| `data[].Service_Line_Items[].List_Price` | body | `number` | no |
| `data[].Service_Line_Items[].Part_Line_Items[].Part` | body | `string` | no |
| `data[].Service_Line_Items[].Part_Line_Items[].Quantity` | body | `number` | no |
| `data[].Service_Line_Items[].Part_Line_Items[].Sequence` | body | `number` | no |
| `data[].Service_Line_Items[].Quantity` | body | `number` | no |
| `data[].Service_Line_Items[].Sequence` | body | `number` | no |
| `data[].Service_Line_Items[].Service` | body | `string` | no |
| `data[].Service_Line_Items[].Service_Tasks_Line_Items[].Sequence` | body | `number` | no |
| `data[].Service_Line_Items[].Service_Tasks_Line_Items[].Service_Task` | body | `string` | no |
| `data[].Service_Line_Items[].Service_Tasks_Line_Items[].ServiceTask_Name` | body | `string` | no |
| `data[].Service_Line_Items[].Status` | body | `string` | no |
| `data[].Service_Line_Items[].Tax.Tax_Exemption_Code` | body | `string` | no |
| `data[].Service_Line_Items[].Tax.Tax_Exemption_Id` | body | `string` | no |
| `data[].Service_Line_Items[].Tax.Tax_Id` | body | `string` | no |
| `data[].Service_Line_Items[].Tax.Tax_Name` | body | `string` | no |
| `data[].Service_Line_Items[].Tax.Tax_Percentage` | body | `string` | no |
| `data[].Service_Line_Items[].Unit` | body | `string` | no |
| `data[].Sub_Total` | body | `number` | no |
| `data[].Summary` | body | `string` | no |
| `data[].Tax_Amount` | body | `string` | no |
| `data[].Territory` | body | `string` | no |
| `data[].Type` | body | `string` | no |
