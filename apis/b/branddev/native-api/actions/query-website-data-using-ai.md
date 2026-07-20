# Query Website Data Using AI with Brand.dev

Retrieves website answers using AI in Brand.dev.

## Endpoint

- **Method:** `POST`
- **Path:** `/brand/ai/query`
- **Base URL:** `https://api.brand.dev/v1`
- **Official documentation:** [Query Website Data Using AI](https://docs.context.dev/api-reference/ai-data-extraction/query-website-data-using-ai)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data_to_extract[]` | body | `array<object>` | yes | Array of data points to extract from the website. |
| `domain` | body | `string` | yes | Domain name to analyze. |
