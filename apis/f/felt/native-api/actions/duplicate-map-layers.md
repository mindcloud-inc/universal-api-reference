# Duplicate Map Layers with Felt

Creates duplicated map layers in Felt.

## Endpoint

- **Method:** `POST`
- **Path:** `/duplicate_layers`
- **Base URL:** `https://felt.com/api/v2`
- **Official documentation:** [Duplicate Map Layers](https://developers.felt.com/rest-api/api-reference/layers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `duplicates[]` | body | `array<object>` | yes | Layer duplication requests with source and destination map IDs. |
