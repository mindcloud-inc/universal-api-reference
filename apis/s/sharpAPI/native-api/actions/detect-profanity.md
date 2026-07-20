# Detect Profanity with SharpAPI

Creates a profanity detection job in SharpAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/content/detect_profanities`
- **Base URL:** `https://sharpapi.com/api/v1`
- **Official documentation:** [Detect Profanity](https://sharpapi.com/en/catalog/ai/content-marketing-automation/profanity-detector)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Provide the text content to analyze for profanity. |
