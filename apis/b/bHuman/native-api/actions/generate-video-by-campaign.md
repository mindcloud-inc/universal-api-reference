# Generate Video by Campaign with BHuman

Creates personalized videos from a campaign in BHuman.

## Endpoint

- **Method:** `POST`
- **Path:** `/ai_studio/pipeline/campaign`
- **Base URL:** `https://studio.bhuman.ai/api`
- **Official documentation:** [Generate Video by Campaign](https://github.com/bhuman-ai/public_api#api-endpoints)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assetsJson` | body | `string` | no | Optional JSON string for the assets matrix. |
| `backgroundsJson` | body | `string` | no | Optional JSON string for the backgrounds array. |
| `callback_url` | body | `string` | no | Optional callback URL for async delivery. |
| `campaign_id` | body | `string` | yes | The campaign ID to generate from. |
| `namesJson` | body | `string` | yes | JSON string for the required nested names array. |
| `variablesJson` | body | `string` | yes | JSON string for the required variables array. |
