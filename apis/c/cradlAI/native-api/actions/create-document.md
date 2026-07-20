# Create Document with Cradl AI

Creates a new document in Cradl AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents`
- **Base URL:** `https://api.cradl.ai/v1`
- **Official documentation:** [Create Document](https://docs.cradl.ai/api-reference/post-documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Document name. |
| `description` | body | `string` | no | Document description. |
| `datasetId` | body | `string` | no | Dataset identifier. |
| `contentType` | body | `string` | no | Document content type. |
| `content` | body | `string` | no | Document content payload. |
| `groundTruth[]` | body | `array<object>` | no | Ground truth labels for the document. |
| `metadata` | body | `object` | no | Metadata attached to the document. |
| `consentId` | body | `string` | no | Consent identifier for the document. |
| `retentionInDays` | body | `number` | no | Retention period in days. |
| `agentRunId` | body | `string` | no | Associated agent run identifier. |
