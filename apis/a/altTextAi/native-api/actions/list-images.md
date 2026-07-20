# List Images with AltText.Ai

Retrieves images from your AltText.Ai library.

## Endpoint

- **Method:** `GET`
- **Path:** `/images`
- **Base URL:** `https://alttext.ai/api/v1`
- **Official documentation:** [List Images](https://alttext.ai/apidocs#tag/Images/operation/get-images)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | no | Return only images whose URL exactly matches this value. |
