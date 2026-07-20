# List Subscriptions with Feedbin

Retrieves a list of subscriptions from Feedbin.

## Endpoint

- **Method:** `GET`
- **Path:** `subscriptions.json`
- **Base URL:** `https://api.feedbin.com/v2`
- **Official documentation:** [List Subscriptions](https://github.com/feedbin/feedbin-api/blob/master/content/subscriptions.md#get-subscriptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `since` | query | `date` | no | Return subscriptions created after this ISO 8601 timestamp. |
| `mode` | query | `string` | no | Use extended to include additional subscription metadata. |
