# Create Hook with Referral Rock

Creates a webhook subscription in Referral Rock.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/hooks`
- **Base URL:** `https://api.referralrock.com`
- **Official documentation:** [Create Hook](https://api.referralrock.com/Help/Api/POST-api-hooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target_url` | body | `string` | yes | The URL to call when the subscribed event occurs. |
| `event` | body | `string` | yes | The Referral Rock event to subscribe to. |
