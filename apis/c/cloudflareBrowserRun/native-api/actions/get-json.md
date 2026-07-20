# Get JSON with Cloudflare Browser Run

Retrieves structured JSON from Cloudflare Browser Run.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/browser-rendering/json`
- **Base URL:** `https://api.cloudflare.com/client/v4`
- **Official documentation:** [Get JSON](https://developers.cloudflare.com/browser-rendering/rest-api/json-endpoint/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `html` | body | `string` | no | HTML content to render. Either HTML or URL must be set. |
| `url` | body | `string` | no | URL to navigate to. Either URL or HTML must be set. |
| `prompt` | body | `string` | no | Prompt to use for JSON extraction. Pass prompt or response format fields as documented. |
| `response_format` | body | `object` | no | Workers AI JSON-mode response format object with type and optional json_schema. |
| `custom_ai[]` | body | `array<object>` | no | Optional ordered list of custom AI model configurations for JSON extraction. |
| `cacheTTL` | query | `number` | no | Cache TTL in seconds. Set 0 to disable cache. |
