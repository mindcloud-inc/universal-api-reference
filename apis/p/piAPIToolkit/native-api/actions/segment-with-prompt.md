# Segment With Prompt API with PiAPI/Toolkit

Creates a prompt-based segmentation task in PiAPI/Toolkit.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Segment With Prompt API](https://piapi.ai/docs/image-editing-api/segment-with-prompt-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.image` | body | `string` | yes | Doc-backed PiAPI field for Segment With Prompt API. |
| `input.prompt` | body | `string` | yes | Doc-backed PiAPI field for Segment With Prompt API. |
| `input.negative_prompt` | body | `string` | no | Doc-backed PiAPI field for Segment With Prompt API. |
| `input.segment_factor` | body | `number` | no | Doc-backed PiAPI field for Segment With Prompt API. |
