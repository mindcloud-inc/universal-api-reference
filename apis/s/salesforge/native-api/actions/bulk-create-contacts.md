# Bulk Create Contacts with Salesforge

Creates contacts in bulk in Salesforge.

## Endpoint

- **Method:** `POST`
- **Path:** `/public/v2/workspaces/:workspaceID/contacts/bulk`
- **Base URL:** `https://api.salesforge.ai`
- **Official documentation:** [Bulk Create Contacts](https://api.salesforge.ai/public/v2/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceID` | path | `string` | yes | — |
| `contacts[]` | body | `array<object>` | yes | — |
| `contacts[].firstName` | body | `string` | yes | — |
| `contacts[].lastName` | body | `string` | no | — |
| `contacts[].email` | body | `string` | no | — |
| `contacts[].company` | body | `string` | no | — |
| `contacts[].position` | body | `string` | no | — |
| `contacts[].linkedinUrl` | body | `string` | no | — |
| `contacts[].tagIds[]` | body | `array<string>` | no | — |
| `contacts[].tags[]` | body | `array<string>` | no | — |
| `contacts[].customVars` | body | `object` | no | Map of custom variable keys to string values for each contact. |
