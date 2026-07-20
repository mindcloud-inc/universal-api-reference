# Create Subscription with Feedbin

Creates a new subscription in Feedbin.

## Endpoint

- **Method:** `POST`
- **Path:** `subscriptions.json`
- **Base URL:** `https://api.feedbin.com/v2`
- **Official documentation:** [Create Subscription](https://github.com/feedbin/feedbin-api/blob/master/content/subscriptions.md#create-subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `feed_url` | body | `string` | yes | Fully qualified feed URL, website URL, hostname, or search text to subscribe to. |
