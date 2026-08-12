# Add Work Order Site Address with Viewpoint Spectrum

## Endpoint

- **Method:** `POST`
- **Path:** `ws/AddWOSiteAddress`
- **Base URL:** `{url}:8482/`
- **Official documentation:** [Add Work Order Site Address](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-payable-services/add-vendor-invoices)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `text/xml; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `Site_ID` | body | `string` | no |
| `Site_Name` | body | `string` | no |
| `Site_Address1` | body | `string` | no |
| `Site_Address2` | body | `string` | no |
| `Site_City` | body | `string` | no |
| `Site_State` | body | `string` | no |
| `Site_Zip_Code` | body | `string` | no |
| `Site_Phone1` | body | `string` | no |
| `Site_Phone2` | body | `string` | no |
| `Telephone_Ext_1` | body | `string` | no |
| `Telephone_Ext_2` | body | `string` | no |
| `Site_Contact_Person` | body | `string` | no |
| `Site_Customer_Code` | body | `string` | no |
| `Lead_Source` | body | `string` | no |
| `Requested_Tech` | body | `string` | no |
| `WO_Type` | body | `string` | no |
| `Zone` | body | `string` | no |
| `Special_Instructions` | body | `string` | no |
| `Show_Notes` | body | `string` | no |
| `Sales_Tax_Code` | body | `string` | no |
| `Taxable_Flag` | body | `string` | no |
| `Labor_Taxable` | body | `string` | no |
| `Material_Taxable` | body | `string` | no |
| `Work_Comp_Code` | body | `string` | no |
| `Wage_Rate_Level` | body | `string` | no |
| `Work_State_Tax_Code` | body | `string` | no |
| `Work_County_Tax_Code` | body | `string` | no |
| `Work_Local_Tax_Code` | body | `string` | no |
| `Work_Site_Email` | body | `string` | no |
| `Site_Case_Type` | body | `string` | no |
| `Customer_Job` | body | `string` | no |
| `Latitude` | body | `string` | no |
| `Longitude` | body | `string` | no |
| `Markup_Code` | body | `string` | no |
| `Alternate_Address` | body | `string` | no |
| `Billto_Code` | body | `string` | no |
| `Cost_Center` | body | `string` | no |
