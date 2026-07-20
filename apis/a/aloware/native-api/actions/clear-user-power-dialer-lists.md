# Clear User Power Dialer Lists with Aloware

Clears all contacts from an Aloware user's power dialer lists.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/webhook/powerdialer-clear-user-lists`
- **Base URL:** `https://app.aloware.com`
- **Official documentation:** [Clear User Power Dialer Lists](https://support.aloware.com/en/articles/9167815-aloware-power-dialer-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | body | `string` | yes | User whose power dialer lists you want to clear. |
