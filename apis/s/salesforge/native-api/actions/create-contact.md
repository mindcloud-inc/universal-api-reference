# Create Contact with Salesforge

Creates a contact in Salesforge.

## Endpoint

- **Method:** `POST`
- **Path:** `/public/v2/workspaces/:workspaceID/contacts`
- **Base URL:** `https://api.salesforge.ai`
- **Official documentation:** [Create Contact](https://api.salesforge.ai/public/v2/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceID` | path | `string` | yes | — |
| `firstName` | body | `string` | yes | — |
| `lastName` | body | `string` | no | — |
| `email` | body | `string` | no | — |
| `company` | body | `string` | no | — |
| `position` | body | `string` | no | — |
| `linkedinUrl` | body | `string` | no | — |
| `tagIds[]` | body | `array<string>` | no | — |
| `tags[]` | body | `array<string>` | no | — |
| `customVars` | body | `object` | no | Map of custom variable keys to string values. |
