# Create Monitor with Exa

Creates a new monitor in Exa.

## Endpoint

- **Method:** `POST`
- **Path:** `/monitors`
- **Base URL:** `https://api.exa.ai`
- **Official documentation:** [Create Monitor](https://exa.ai/docs/websets/api/monitors/create-a-monitor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `metadata` | body | `object` | no | Optional key-value metadata object. |
| `name` | body | `string` | no | Optional display name for the monitor. |
| `outputSchema` | body | `object` | no | Optional JSON schema for structured monitor output. |
| `search.contents` | body | `object` | no | Optional content extraction configuration object. |
| `search.numResults` | body | `number` | no | Number of results to retrieve per run. |
| `search.query` | body | `string` | yes | Search query to run on every monitor execution. |
| `trigger.period` | body | `string` | no | Interval duration like 1h, 6h, 1d, or 7d. |
| `trigger.type` | body | `string` | no | Use interval when scheduling the monitor. |
| `webhook.events[]` | body | `array<string>` | no | Optional list of monitor events to deliver. |
| `webhook.url` | body | `string` | yes | HTTPS URL that receives monitor events. |
