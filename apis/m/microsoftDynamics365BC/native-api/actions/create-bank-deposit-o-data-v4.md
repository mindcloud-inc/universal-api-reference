# Create Bank Deposit ODataV4 with Microsoft Dynamics 365 BC

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/ODataV4/Company(:company)/MindcloudBankDepositHeader`
- **Base URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/`
- **API:** REST

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `company` | path | `list` | no |
| `Bank_Account_No` | body | `string` | no |
