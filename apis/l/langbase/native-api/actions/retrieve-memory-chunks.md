# Retrieve Memory Chunks with Langbase

## Endpoint

- **Method:** `POST`
- **Path:** `v1/memory/retrieve`
- **Base URL:** `https://api.langbase.com`
- **Official documentation:** [Retrieve Memory Chunks](https://langbase.com/docs/api-reference/memory/retrieve)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `memory[]` | body | `array<object>` | yes | Array of memory selectors to search. |
| `query` | body | `string` | yes | Question or text to retrieve against the selected memories. |
