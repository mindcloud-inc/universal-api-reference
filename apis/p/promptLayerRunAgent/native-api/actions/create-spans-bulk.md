# Create Spans Bulk with PromptLayer Run Agent

Creates spans in bulk in PromptLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/spans-bulk`
- **Base URL:** `https://api.promptlayer.com`
- **Official documentation:** [Create Spans Bulk](https://docs.promptlayer.com/reference/spans-bulk)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spans[]` | body | `array<object>` | yes | Array of span objects to create in PromptLayer. |
