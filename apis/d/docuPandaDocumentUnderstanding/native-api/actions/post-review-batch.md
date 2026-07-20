# Generate a Visual Review with DocuPanda - Document Understanding

Creates a visual review in DocuPanda.

## Endpoint

- **Method:** `POST`
- **Path:** `/review/batch`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Generate a Visual Review](https://docs.docupipe.ai/reference/post_review_batch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `standardizationIds` | body | `list<string>` | yes | Unique identifier of the standardization object. |
| `standardizationIds[]` | body | `array<string>` | yes | Unique identifier of the standardization object. |
| `reviewInstructions` | body | `string` | no | — |
| `highGranularity` | body | `boolean` | no | When enabled, the review will locate individual sub-fields within compound items (e.g. each field within a line item). This provides more precise bounding boxes but costs 4 credits/page instead of 2. |
