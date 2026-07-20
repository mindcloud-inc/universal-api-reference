# Generate Image with Soul Standard with Higgsfield AI

Creates an image with Soul Standard in Higgsfield AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/higgsfield-ai/soul/standard`
- **Base URL:** `https://platform.higgsfield.ai`
- **Official documentation:** [Generate Image with Soul Standard](https://docs.higgsfield.ai/guides/images)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | Text prompt describing the image to generate. |
| `aspect_ratio` | body | `string` | no | Generation aspect ratio, for example 16:9. |
| `resolution` | body | `string` | no | Generation resolution, for example 720p. |
| `hf_webhook` | query | `string` | no | Optional public webhook URL for final generation status notifications. |
