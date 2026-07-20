# Delete Hook with Referral Rock

Deletes a webhook subscription from Referral Rock.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/hooks`
- **Base URL:** `https://api.referralrock.com`
- **Official documentation:** [Delete Hook](https://api.referralrock.com/Help/Api/DELETE-api-hooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `web_hook_id` | body | `string` | yes | The unique ID of the webhook subscription to remove. |
