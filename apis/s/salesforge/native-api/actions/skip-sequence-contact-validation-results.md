# Skip Sequence Contact Validation Results with Salesforge

Skips sequence contact validation results in Salesforge.

## Endpoint

- **Method:** `POST`
- **Path:** `/public/v2/workspaces/:workspaceID/sequences/:sequenceID/contacts/validation/skip`
- **Base URL:** `https://api.salesforge.ai`
- **Official documentation:** [Skip Sequence Contact Validation Results](https://api.salesforge.ai/public/v2/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceID` | path | `string` | yes | Workspace ID for the sequence. |
| `sequenceID` | path | `string` | yes | Sequence ID with validation results to skip. |
