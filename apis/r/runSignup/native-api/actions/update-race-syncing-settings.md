# Update Race Syncing Settings with RunSignup

## Endpoint

- **Method:** `POST`
- **Path:** `/race/:race_id/sync-settings`
- **Base URL:** `https://api.runsignup.com/rest`
- **Official documentation:** [Update Race Syncing Settings](https://runsignup.com/API/race/:race_id/sync-settings/POST)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `race_id` | path | `string` | yes | Path parameter: race_id |
| `safe_sync_enabled` | body | `string` | no | — |
