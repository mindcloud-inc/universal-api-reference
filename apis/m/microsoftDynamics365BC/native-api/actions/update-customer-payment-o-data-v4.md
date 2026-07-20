# Update Customer Payment ODataV4 with Microsoft Dynamics 365 BC

## Endpoint

- **Method:** `PATCH`
- **Path:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/ODataV4/Company(:company)/Cash_Receipt_Journals_Excel(Journal_Template_Name=':journalTemplateName',Journal_Batch_Name=':journalBatchName',Line_No=:lineNo)`
- **Base URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/`
- **API:** REST

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `company` | path | `list` | no |
| `Description` | body | `string` | no |
| `Document_Date` | body | `string` | no |
| `External_Document_No` | body | `string` | no |
| `Payment_Method_Code` | body | `string` | no |
| `Account_No` | body | `string` | no |
| `Amount` | body | `number` | no |
| `lineNo` | path | `number` | no |
| `journalBatchName` | path | `string` | no |
| `journalTemplateName` | path | `string` | no |
| `odataetag` | body | `string` | no |
| `Bal_Account_No` | body | `string` | no |
| `Bal_Account_Type` | body | `string` | no |
