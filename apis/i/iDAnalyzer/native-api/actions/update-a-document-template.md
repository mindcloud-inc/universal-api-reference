# Update a document template with ID Analyzer

Updates a document template in ID Analyzer.

## Endpoint

- **Method:** `POST`
- **Path:** `/contract/:templateId`
- **Base URL:** `https://api2.idanalyzer.com`
- **Official documentation:** [Update a document template](https://developer.idanalyzer.com/reference/post-contract-templateid-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Updated HTML template content. |
| `name` | body | `string` | yes | Template name required by the provider when updating template content. |
| `templateId` | path | `string` | yes | Stored template ID. |
