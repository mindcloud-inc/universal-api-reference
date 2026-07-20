# Create Subscription with Signaturit

Creates a new subscription in Signaturit.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscriptions.json`
- **Base URL:** `https://api.sandbox.signaturit.com/v3`
- **API:** rest
- **Official documentation:** [Create Subscription](https://docs.signaturit.com/api/latest#subscriptions_post_subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Destination URL that will receive Signaturit event payloads. |
| `events` | body | `string` | yes | Signaturit event code to subscribe to. |
