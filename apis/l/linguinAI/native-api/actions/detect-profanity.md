# Detect Profanity with Linguin AI

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/detect/profanity`
- **Base URL:** `https://api.linguin.ai`
- **Official documentation:** [Detect Profanity](https://linguin.ai/api-docs/v2/#single-profanity-detection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | body | `string` | yes | The text to analyze for profanity. |
