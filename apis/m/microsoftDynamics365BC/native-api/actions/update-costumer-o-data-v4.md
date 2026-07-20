# Update Costumer ODataV4 with Microsoft Dynamics 365 BC

## Endpoint

- **Method:** `PATCH`
- **Path:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/ODataV4/Company(:companyId)/MindcloudCustomerCard(':customerId')`
- **Base URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/`
- **API:** REST
- **Official documentation:** [Update Costumer ODataV4](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_customer_update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `County` | body | `string` | no |
| `Post_Code` | body | `string` | no |
| `Country_Region_Code` | body | `string` | no |
| `Search_Name` | body | `string` | no |
| `Salesperson_Code` | body | `string` | no |
| `city` | body | `string` | no |
| `Payment_Terms_Code` | body | `string` | no |
| `Customer_Posting_Group` | body | `string` | no |
| `Gen_Bus_Posting_Group` | body | `string` | no |
| `Tax_Area_Code` | body | `string` | no |
| `Tax_Liable` | body | `boolean` | no |
| `Address` | body | `string` | no |
| `companyId` | path | `list` | no |
| `customerId` | path | `string` | no |
| `E_Mail` | body | `string` | no |
| `Name` | body | `string` | no |
| `Phone_No` | body | `string` | no |
