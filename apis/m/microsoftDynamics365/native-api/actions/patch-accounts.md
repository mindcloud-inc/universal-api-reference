# Patch Accounts with Microsoft Dynamics 365

## Endpoint

- **Method:** `PATCH`
- **Path:** `/accounts(:accountsId)`
- **Base URL:** `{baseURL}`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customFields[]` | body | `array` | no |
| `customFields[].customKey` | body | `string` | no |
| `accountsId` | path | `string` | no |
| `customFields[].customValue` | body | `string` | no |
