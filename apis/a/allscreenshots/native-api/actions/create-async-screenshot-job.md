# Create Async Screenshot Job with Allscreenshots

Creates a new async screenshot job in Allscreenshots.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/screenshots/async`
- **Base URL:** `https://api.allscreenshots.com`
- **Official documentation:** [Create Async Screenshot Job](https://docs.allscreenshots.com/api-reference/async-jobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The webpage URL to capture asynchronously. |
| `format` | body | `string` | no | Output format such as png, jpeg, webp, or pdf. |
| `fullPage` | body | `boolean` | no | Capture the full scrollable page instead of the visible viewport. |
| `responseType` | body | `string` | no | How the finished job result should be returned. |
| `webhookUrl` | body | `string` | no | Optional URL to notify when the async job completes. |
| `webhookSecret` | body | `string` | no | Optional secret used to sign webhook deliveries. |
| `outputs[]` | body | `array<object>` | no | Optional multi-output extraction configuration. |
