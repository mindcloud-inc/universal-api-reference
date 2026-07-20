# Rerank Documents with SEA-LION AI Playground

## Endpoint

- **Method:** `POST`
- **Path:** `/rerank`
- **Base URL:** `https://api.sea-lion.ai/v1`
- **Official documentation:** [Rerank Documents](https://api.sea-lion.ai/openapi.json)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `model` | body | `string` | yes |
| `query` | body | `string` | yes |
| `documents[]` | body | `array<string>` | yes |
