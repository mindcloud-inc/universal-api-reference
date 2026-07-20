# Create Webhook with Fathom

Creates a new webhook in Fathom.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://api.fathom.ai/external/v1`
- **Official documentation:** [Create Webhook](https://developers.fathom.ai/api-reference/webhooks/create-a-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `destination_url` | body | `string` | yes | Webhook destination URL. |
| `triggered_for[]` | body | `array<string>` | yes | One or more webhook scopes. Allowed: my_recordings, shared_with_me, internal_meetings, external_meetings, all_recordings. Accepted values: `0`, `1`, `2`, `3`, `4`. |
| `include_action_items` | body | `boolean` | no | Include action items in webhook payload. |
| `include_crm_matches` | body | `boolean` | no | Include CRM matches in webhook payload. |
| `include_summary` | body | `boolean` | no | Include summary in webhook payload. |
| `include_transcript` | body | `boolean` | no | Include transcript in webhook payload. |
