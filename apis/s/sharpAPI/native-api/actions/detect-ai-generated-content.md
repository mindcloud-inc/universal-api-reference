# Detect Ai Generated Content with SharpAPI

Creates an AI content detection job in SharpAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/content/detect_ai`
- **Base URL:** `https://sharpapi.com/api/v1`
- **Official documentation:** [Detect Ai Generated Content](https://sharpapi.com/en/catalog/ai/content-marketing-automation/ai-content-detector)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Provide the text content to analyze for AI-generated patterns. |
