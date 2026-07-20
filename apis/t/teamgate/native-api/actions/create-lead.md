# Create Lead with Teamgate

Creates a new lead in Teamgate.

## Endpoint

- **Method:** `POST`
- **Path:** `/leads`
- **Base URL:** `https://api.teamgate.com/v4`
- **Official documentation:** [Create Lead](https://developers.teamgate.com/#8921df2b-3158-4b16-b81c-c37c6414c20f)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Lead name. |
| `companyName` | body | `string` | no | Company name when linking or creating lead company context. |
| `companyId` | body | `string` | no | Existing company ID to link to the lead. |
| `jobTitle` | body | `string` | no | Lead job title. |
| `statusId` | body | `string` | no | Lead status ID. |
| `starred` | body | `string` | no | Whether the lead is starred. Use Teamgate values like yes or no. |
| `ownerId` | body | `string` | no | Owner user ID. |
| `ownerUsername` | body | `string` | no | Owner username. |
| `source` | body | `string` | no | Lead source name. |
| `sourceDescription` | body | `string` | no | Lead source description. |
| `industry` | body | `string` | no | Lead industry name. |
| `industryDescription` | body | `string` | no | Lead industry description. |
| `tags` | body | `string` | no | Lead tags. |
