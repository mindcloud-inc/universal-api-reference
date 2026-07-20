# Generate Alt Text for Image with AltText.Ai

Generates alt text for a new image in AltText.Ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/images`
- **Base URL:** `https://alttext.ai/api/v1`
- **Official documentation:** [Generate Alt Text for Image](https://alttext.ai/apidocs#tag/Images/operation/create-image)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `async` | body | `boolean` | no | When true, queue the image for background processing and return immediately. |
| `gpt_prompt` | body | `string` | no | Optional English prompt containing `{{AltText}}` to rewrite the generated alt text. |
| `image` | body | `object` | yes | The image payload. Provide either a public `url` or base64 `raw` image data, with optional `asset_id`, `tags`, or `metadata` inside this object. |
| `keyword_source` | body | `string` | no | Source text to mine for keywords when you do not provide the `keywords` array. |
| `keywords[]` | body | `array<string>` | no | Optional SEO keywords or phrases for the generated alt text. |
| `lang` | body | `string` | no | One or more language codes, such as `en` or `en,es,fr`, for generated alt text. |
| `max_chars` | body | `number` | no | Limit the generated alt text length between 80 and 500 characters. |
| `model_name` | body | `string` | no | Choose the AltText.ai language model, such as `describe-regular` or `describe-terse`. |
| `overwrite` | body | `boolean` | no | When true, regenerate alt text for an existing image with the same URL or asset ID. |
| `timeout_secs` | body | `number` | no | Maximum seconds to wait for generation, between 5 and 30. |
| `webhook_url` | body | `string` | no | Optional webhook URL override for this request. |
