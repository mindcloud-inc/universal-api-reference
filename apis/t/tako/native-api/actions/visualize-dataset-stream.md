# Visualize Dataset Stream with Tako

Creates a knowledge card from your dataset in Tako as a stream.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/beta/visualize/stream`
- **Base URL:** `https://tako.com/api`
- **Official documentation:** [Visualize Dataset Stream](https://docs.tako.com/api-reference/visualize-stream)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_ids[]` | body | `array<string>` | no | One or more connected Tako file IDs to visualize in the streaming pipeline. |
| `query` | body | `string` | no | Optional instructions describing the streaming visualization you want Tako to create. |
