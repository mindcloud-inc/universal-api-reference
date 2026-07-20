# Summarize Text with Sapling

Summarizes input text into shorter output with Sapling.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/summarize`
- **Base URL:** `https://api.sapling.ai`
- **Official documentation:** [Summarize Text](https://sapling.ai/docs/api/summarize/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | Input document to summarize. |
