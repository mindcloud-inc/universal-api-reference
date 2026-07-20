# Create Slide with Alai

Creates an async slide generation in an Alai presentation.

## Endpoint

- **Method:** `POST`
- **Path:** `/presentations/:presentation_id/slides`
- **Base URL:** `https://slides-api.getalai.com/api/v1`
- **Official documentation:** [Create Slide](https://docs.getalai.com/api/create-slide)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `presentation_id` | path | `string` | yes | Target presentation identifier. |
| `slide_context` | body | `string` | yes | Content for the new slide. |
| `options.additional_instructions` | body | `string` | no | Optional slide styling or layout guidance. |
| `options.slide_order` | body | `number` | no | Optional position index for the new slide. |
