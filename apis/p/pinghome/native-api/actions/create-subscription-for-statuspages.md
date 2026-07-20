# Create Subscription For Statuspages with Pinghome

Creates a new statuspage subscription in Pinghome.

## Endpoint

- **Method:** `POST`
- **Path:** `/statuspage-cmd/v1/subscriptions`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [Create Subscription For Statuspages](https://docs.pinghome.io/statuspages/create-subscription-for-statuspages/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel_type` | body | `string` | yes | Notification channel type. |
| `domain` | body | `string` | no | Statuspage domain or subdomain used to locate the statuspage for the subscription. |
| `channel_value` | body | `string` | yes | Notification channel value. |
