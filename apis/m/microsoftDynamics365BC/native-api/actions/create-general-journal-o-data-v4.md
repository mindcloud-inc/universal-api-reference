# Create General Journal ODataV4 with Microsoft Dynamics 365 BC

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/ODataV4/Company(:company)/MindcloudGeneralJournal`
- **Base URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/`
- **API:** REST

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `company` | path | `list` | no |
| `Description` | body | `string` | no |
| `Document_Type` | body | `string` | no |
| `External_Document_No` | body | `string` | no |
| `Payment_Method_Code` | body | `string` | no |
| `Account_No` | body | `string` | no |
| `Amount` | body | `number` | no |
| `Account_Type` | body | `string` | no |
| `Line_No` | body | `number` | no |
| `Journal_Batch_Name` | body | `string` | no |
| `Journal_Template_Name` | body | `string` | no |
| `Bal_Account_No` | body | `string` | no |
| `Bal_Account_Type` | body | `string` | no |
| `Applies_to_Doc_Type` | body | `string` | no |
| `Document_No` | body | `string` | no |
| `Posting_Date` | body | `string` | no |
| `Applies_to_Doc_No` | body | `string` | no |
| `Line_Type` | body | `string` | no |
| `Shortcut_Dimension_1_Code` | body | `string` | no |
| `Comment` | body | `string` | no |
| `Gen_Prod_Posting_Group` | body | `string` | no |
| `Bal_Gen_Prod_Posting_Group` | body | `string` | no |
| `Shortcut_Dimension_2_Code` | body | `string` | no |
