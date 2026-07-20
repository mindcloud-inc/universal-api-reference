# Review Document With Human Review Config with Google Cloud Document AI

Creates a human review request in Google Cloud Document AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/projects/:projectsId/locations/:locationsId/processors/:processorsId/humanReviewConfig:reviewDocument`
- **Base URL:** `https://documentai.googleapis.com`
- **Official documentation:** [Review Document With Human Review Config](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.processors.humanReviewConfig/reviewDocument)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `processorsId` | path | `string` | yes | Document AI processor ID. |
| `inlineDocument` | body | `object` | yes | Document to send for human review. |
| `enableSchemaValidation` | body | `boolean` | no | Whether to validate the document against the schema. |
| `priority` | body | `string` | no | Review priority. |
| `documentSchema` | body | `object` | no | Optional schema to use for validation. |
