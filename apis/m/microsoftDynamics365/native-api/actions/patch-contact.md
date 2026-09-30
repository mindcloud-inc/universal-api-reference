# Patch Contact with Microsoft Dynamics 365

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contacts(:contactId)`
- **Base URL:** `{baseURL}`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customFields[]` | body | `array` | no |
| `customFields[].customKey` | body | `string` | no |
| `contactId` | path | `string` | no |
| `customFields[].customValue` | body | `string` | no |
