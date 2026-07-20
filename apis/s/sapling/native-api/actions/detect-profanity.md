# Detect Profanity with Sapling

Detects profanity in text with Sapling.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/profanity`
- **Base URL:** `https://api.sapling.ai`
- **Official documentation:** [Detect Profanity](https://sapling.ai/docs/api/profanity/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | Text to check for profanity. |
