# Create Bank Deposit Lines ODataV4 with Microsoft Dynamics 365 BC

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/ODataV4/Company(:company)/MindcloudBankDepositLines`
- **Base URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/`
- **API:** REST

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `company` | path | `list` | no |
| `Bank_Deposit_No` | body | `string` | no |
| `Account_Type` | body | `string` | no |
| `Account_No` | body | `string` | no |
| `Document_Type` | body | `string` | no |
| `Document_No` | body | `string` | no |
| `External_Document_No` | body | `string` | no |
| `Description` | body | `string` | no |
| `Credit_Amount` | body | `string` | no |
