# Create Alias with Mixpanel

Creates a user identity alias in Mixpanel.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.mixpanel.com/track`
- **Base URL:** `https://mixpanel.com/api`
- **Official documentation:** [Create Alias](https://developer.mixpanel.com/reference/identity-create-alias)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `distinct_id` | body | `string` | yes | Existing distinct ID that should gain a new alias. |
| `alias` | body | `string` | yes | New alias that Mixpanel should interpret as the existing distinct ID. |
| `strict` | body | `string` | no | When 1, Mixpanel validates the alias payload and returns per-record validation errors. |
