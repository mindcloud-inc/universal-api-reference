# Import Lead To Sequence with Salesforge

Imports a lead to a sequence in Salesforge.

## Endpoint

- **Method:** `PUT`
- **Path:** `/public/v2/workspaces/:workspaceID/sequences/:sequenceID/import-lead`
- **Base URL:** `https://api.salesforge.ai`
- **Official documentation:** [Import Lead To Sequence](https://api.salesforge.ai/public/v2/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceID` | path | `string` | yes | Workspace ID for the sequence. |
| `sequenceID` | path | `string` | yes | Sequence ID to import the lead into. |
| `firstName` | body | `string` | yes | Lead first name. |
| `lastName` | body | `string` | no | Lead last name. |
| `email` | body | `string` | no | Lead email address. |
| `company` | body | `string` | no | Lead company name. |
| `position` | body | `string` | no | Lead job title. |
| `linkedinUrl` | body | `string` | no | Lead LinkedIn profile URL. |
| `tags[]` | body | `array<string>` | no | Tags to apply to the lead. |
| `tagIds[]` | body | `array<string>` | no | Existing tag IDs to apply to the lead. |
