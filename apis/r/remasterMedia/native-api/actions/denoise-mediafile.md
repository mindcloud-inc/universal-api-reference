# Denoise Mediafile with RemasterMedia

Creates a denoised mediafile in RemasterMedia using a preset.

## Endpoint

- **Method:** `POST`
- **Path:** `/mediafiles/process`
- **Base URL:** `https://api-sandbox.remastermedia.com/v2`
- **Official documentation:** [Denoise Mediafile](https://remastermedia-web-assets.s3-accelerate.amazonaws.com/api_reference-v2.html#mediafiles-process-mediafile-post-3)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source_id` | body | `string` | yes | ID of the mediafile to denoise. |
| `options.preset` | body | `string` | no | Optional noise-reduction preset name. Direct noise-reduction parameters can be supplied instead. |
| `options.offset` | body | `number` | no | Optional number of seconds to skip from the start. |
| `options.duration` | body | `number` | no | Optional output duration limit in seconds. |
| `options.html5_compatible` | body | `boolean` | no | Whether to create HTML5-compatible output. |
| `options.algorithm` | body | `number` | no | Noise reduction algorithm: 0 for AI Clarity v1, 1 for AI Natural v1. |
| `options.aggressiveness` | body | `number` | no | Noise reduction aggressiveness: 0, 1, or 2. |
| `options.amount` | body | `number` | no | Noise reduction amount as a percentage. |
| `options.gain` | body | `number` | no | Noise reduction gain parameter. |
| `options.lower_bound` | body | `number` | no | Noise reduction lower bound parameter. |
| `webhook_url` | body | `string` | no | Optional webhook URL notified when processing finishes. |
| `user_data` | body | `object` | no | Optional custom object stored with the derived mediafile. |
