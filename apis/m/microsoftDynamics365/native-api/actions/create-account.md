# Create Account with Microsoft Dynamics 365

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts`
- **Base URL:** `{baseURL}`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customFields[].customKey` | body | `string` | no |
| `name` | body | `string` | yes |
| `accountnumber` | body | `string` | no |
| `customFields[].customValue` | body | `string` | no |
| `emailaddress1` | body | `string` | no |
| `telephone1` | body | `string` | no |
| `customFields[]` | body | `array` | no |
