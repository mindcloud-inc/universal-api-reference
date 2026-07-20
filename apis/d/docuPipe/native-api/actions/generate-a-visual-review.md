# Generate a Visual Review with DocuPipe

Creates a visual review in DocuPipe.

## Endpoint

- **Method:** `POST`
- **Path:** `/review/batch`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Generate a Visual Review](https://docs.docupipe.ai/reference/post_review_batch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `standardizationIds[]` | body | `array<string>` | yes | Unique identifier of the standardization object. |
| `reviewInstructions` | body | `string` | no | Instructions for the review process. You may optionally specify which fields you want to localize, and give the AI tips to improve review performance |
| `highGranularity` | body | `boolean` | no | When enabled, the review will locate individual sub-fields within compound items (e.g. each field within a line item). This provides more precise bounding boxes but costs 4 credits/page instead of 2. |
