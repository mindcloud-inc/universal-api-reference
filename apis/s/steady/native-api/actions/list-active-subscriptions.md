# List Active Subscriptions with Steady

Retrieves active subscriptions for a Steady publication.

## Endpoint

- **Method:** `GET`
- **Path:** `/subscriptions`
- **Base URL:** `https://steadyhq.com/api/v1`
- **Official documentation:** [List Active Subscriptions](https://developers.steadyhq.com/#get-subscriptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[subscriber][email]` | query | `string` | no | A URL-encoded comma-separated list of subscriber email addresses to include. |
