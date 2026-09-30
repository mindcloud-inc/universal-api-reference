# Create Contact with Microsoft Dynamics 365

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `{baseURL}`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customFields[].customKey` | body | `string` | no |
| `lastname` | body | `string` | yes |
| `customFields[].customValue` | body | `string` | no |
| `firstname` | body | `string` | no |
| `fullname` | body | `string` | no |
| `emailaddress1` | body | `string` | no |
| `customFields[]` | body | `array` | no |
| `$expand` | query | `string` | no |
| `$select` | query | `string` | no |
