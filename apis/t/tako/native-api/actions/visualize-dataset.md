# Visualize Dataset with Tako

Creates a knowledge card from your dataset in Tako.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/beta/visualize`
- **Base URL:** `https://tako.com/api`
- **Official documentation:** [Visualize Dataset](https://docs.tako.com/api-reference/visualize)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_ids[]` | body | `array<string>` | no | One or more connected Tako file IDs to visualize. |
| `query` | body | `string` | no | Optional instructions describing the visualization you want Tako to create. |
