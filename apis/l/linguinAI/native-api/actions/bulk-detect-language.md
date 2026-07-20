# Bulk Detect Language with Linguin AI

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/bulk_detect/language`
- **Base URL:** `https://api.linguin.ai`
- **Official documentation:** [Bulk Detect Language](https://linguin.ai/api-docs/v2/#bulk-language-detection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q[]` | body | `array<string>` | yes | The texts to analyze for language detection. Send multiple values as a array. |
