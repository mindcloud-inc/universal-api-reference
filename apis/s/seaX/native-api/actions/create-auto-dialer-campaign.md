# Create Auto Dialer Campaign with SeaX

Creates an auto dialer campaign in SeaX.

## Endpoint

- **Method:** `POST`
- **Path:** `/auto_dialer_campaigns`
- **Base URL:** `https://seax.seasalt.ai/seax-api/api/v1/workspace/{workspaceId}`
- **Official documentation:** [Create Auto Dialer Campaign](https://api.seasalt.ai/seax/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `capture_keypress` | body | `boolean` | yes | Whether to capture keypad input. |
| `capture_stt` | body | `boolean` | yes | Whether to capture speech-to-text. |
| `mode` | body | `string` | yes | Auto dialer mode. |
| `name` | body | `string` | yes | Auto dialer campaign name. |
| `phone_ids` | body | `list<string>` | yes | Phone identifiers to call from. |
| `stage` | body | `string` | yes | Auto dialer stage. |
| `type` | body | `string` | yes | Auto dialer campaign type. |
