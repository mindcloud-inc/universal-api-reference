# Create Work Orders with Viewpoint Spectrum

## Endpoint

- **Method:** `POST`
- **Path:** `ws/WorkOrderHeader`
- **Base URL:** `{url}:8482/`
- **Official documentation:** [Create Work Orders](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-payable-services/add-vendor-invoices)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `text/xml; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `WO_Number` | body | `string` | no |
| `WO_Reference_Code` | body | `string` | no |
| `WO_Job_Number` | body | `string` | no |
| `WO_Job_Division` | body | `string` | no |
| `Bill_Customer_Code` | body | `string` | no |
| `contractNumber` | body | `string` | no |
| `Customer_PO_Number` | body | `list` | no |
| `Customer_Job` | body | `date` | no |
| `WO_Phone1` | body | `string` | no |
| `WO_Phone2` | body | `string` | no |
| `Bill_Contract` | body | `number` | no |
| `Zone` | body | `string` | no |
| `Priority_Code` | body | `string` | no |
| `WO_Case_Type` | body | `string` | no |
| `Price_Type` | body | `string` | no |
| `Total_Quote_Amount` | body | `string` | no |
| `Projected_Hours` | body | `string` | no |
| `Est_Arrival` | body | `string` | no |
| `Dispatch_Status_Code` | body | `string` | no |
| `Summary_Description` | body | `string` | no |
| `Ordered_Date` | body | `string` | no |
| `Time_Entered` | body | `string` | no |
| `Requested_Date` | body | `string` | no |
| `Estimated_Complete_Time` | body | `number` | no |
| `Scheduled_Start_Date` | body | `string` | no |
| `Scheduled_Start_Time` | body | `string` | no |
| `Date_Assigned` | body | `string` | no |
| `Time_Assigned` | body | `string` | no |
| `Arrival_Date` | body | `string` | no |
| `Arrival_Time` | body | `string` | no |
| `Complete_Date` | body | `string` | no |
| `Complete_Time` | body | `string` | no |
| `Lead_Source` | body | `string` | no |
| `Sales_Person` | body | `string` | no |
| `Taken_By` | body | `string` | no |
| `AR_Terms_Code` | body | `string` | no |
| `Sales_Tax_Code` | body | `string` | no |
| `Taxable_Flag` | body | `string` | no |
| `GL_Department` | body | `string` | no |
| `Cost_Center` | body | `string` | no |
| `Billto_Code` | body | `string` | no |
| `Override_ERO_Markup` | body | `string` | no |
| `Material_Price_Level` | body | `string` | no |
| `Price_Level` | body | `string` | no |
| `Markup_Code` | body | `string` | no |
