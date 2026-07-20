# Bulk Detect Profanity with Linguin AI

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/bulk_detect/profanity`
- **Base URL:** `https://api.linguin.ai`
- **Official documentation:** [Bulk Detect Profanity](https://linguin.ai/api-docs/v2/#bulk-profanity-detection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q[]` | body | `array<string>` | yes | The texts to analyze for profanity. Send multiple values as a array. |
