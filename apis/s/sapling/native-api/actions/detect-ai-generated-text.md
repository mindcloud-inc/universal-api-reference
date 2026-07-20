# Detect AI-Generated Text with Sapling

Detects whether text is AI-generated with Sapling.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/aidetect`
- **Base URL:** `https://api.sapling.ai`
- **Official documentation:** [Detect AI-Generated Text](https://sapling.ai/docs/api/detector/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | Text to run AI detection on. |
