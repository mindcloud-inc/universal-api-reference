# Create Contents Job with Valyu

## Endpoint

- **Method:** `POST`
- **Path:** `/contents`
- **Base URL:** `https://api.valyu.ai/v1`
- **Official documentation:** [Create Contents Job](https://docs.valyu.ai/guides/content-extraction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `urls[]` | body | `array<string>` | yes | URLs to extract content from. |
| `response_length` | body | `string` | no | Maximum character length of extracted content per URL. |
| `extract_effort` | body | `string` | no | Controls how pages are rendered for extraction. |
| `summary` | body | `string` | no | Optional AI-powered content processing mode. |
