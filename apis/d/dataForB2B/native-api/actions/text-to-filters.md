# Text To Filters with DataForB2B

Converts text into DataForB2B search filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/search/llm/filters`
- **Base URL:** `https://api.dataforb2b.ai`
- **Official documentation:** [Text To Filters](https://docs.dataforb2b.ai/api-reference/text-to-filters)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Natural-language text to convert into structured filters. |
| `category` | body | `string` | yes | Target category for the generated filters, such as people or company. |
