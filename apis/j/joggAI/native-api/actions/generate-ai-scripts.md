# Generate AI Scripts with JoggAI

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/ai_scripts`
- **Base URL:** `https://api.jogg.ai`
- **Official documentation:** [Generate AI Scripts](https://docs.jogg.ai/api-reference/v2/Asset/CreateAIScript)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language` | body | `string` | yes | Script language such as english or spanish |
| `product_info.data.description` | body | `string` | no | Product description when source type is details |
| `product_info.data.id` | body | `string` | no | Existing product ID when source type is id |
| `product_info.data.name` | body | `string` | no | Product name when source type is details |
| `product_info.source_type` | body | `string` | yes | Use id for an existing product or details for manual product details |
| `script_style` | body | `string` | yes | Requested script style |
| `target_audience` | body | `string` | no | Optional target audience description |
| `video_length_seconds` | body | `string` | yes | Desired video length in seconds: 15, 30, or 60 |
