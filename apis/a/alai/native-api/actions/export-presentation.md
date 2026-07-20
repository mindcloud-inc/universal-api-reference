# Export Presentation with Alai

Creates an async presentation export in Alai.

## Endpoint

- **Method:** `POST`
- **Path:** `/presentations/:presentation_id/exports`
- **Base URL:** `https://slides-api.getalai.com/api/v1`
- **Official documentation:** [Export Presentation](https://docs.getalai.com/api/export-presentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `presentation_id` | path | `string` | yes | Target presentation identifier. |
| `formats[]` | body | `array<string>` | yes | Requested export formats. |
