# Update Monitor with Exa

Updates an existing monitor in Exa.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/monitors/:id`
- **Base URL:** `https://api.exa.ai`
- **Official documentation:** [Update Monitor](https://exa.ai/docs/websets/api/monitors/update-monitor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Monitor identifier. |
| `metadata` | body | `object` | no | Updated metadata object. |
| `name` | body | `string` | no | Updated monitor name. |
| `outputSchema` | body | `object` | no | Updated JSON schema for structured output. |
| `search.contents` | body | `object` | no | Updated content extraction configuration object. |
| `search.numResults` | body | `number` | no | Updated result count per run. |
| `search.query` | body | `string` | no | Updated search query. |
| `status` | body | `string` | no | Monitor status: active or paused. |
| `trigger.period` | body | `string` | no | Updated interval duration. |
| `trigger.type` | body | `string` | no | Use interval when scheduling the monitor. |
| `webhook.events[]` | body | `array<string>` | no | Updated list of webhook events. |
| `webhook.url` | body | `string` | no | Updated HTTPS webhook URL. |
