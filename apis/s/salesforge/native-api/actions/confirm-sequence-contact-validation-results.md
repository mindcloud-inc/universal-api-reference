# Confirm Sequence Contact Validation Results with Salesforge

Confirms sequence contact validation results in Salesforge.

## Endpoint

- **Method:** `POST`
- **Path:** `/public/v2/workspaces/:workspaceID/sequences/:sequenceID/contacts/validation/confirm`
- **Base URL:** `https://api.salesforge.ai`
- **Official documentation:** [Confirm Sequence Contact Validation Results](https://api.salesforge.ai/public/v2/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceID` | path | `string` | yes | Workspace ID for the sequence. |
| `sequenceID` | path | `string` | yes | Sequence ID with validation results to confirm. |
| `esps[]` | body | `array<string>` | yes | Email service providers to keep when confirming validation results. |
| `statuses[]` | body | `array<string>` | no | Validation statuses to keep when confirming validation results. |
