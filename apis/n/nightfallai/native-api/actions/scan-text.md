# Scan Text with Nightfall.ai

Scans text for sensitive data with Nightfall.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/scan`
- **Base URL:** `https://api.nightfall.ai`
- **Official documentation:** [Scan Text](https://help.nightfall.ai/developer-api/introduction/quickstart)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `payload[]` | body | `array<string>` | yes | Array of text strings to scan. |
| `policy` | body | `object` | yes | Inline Nightfall policy object with detectionRules or referenced detection rule UUIDs. |
