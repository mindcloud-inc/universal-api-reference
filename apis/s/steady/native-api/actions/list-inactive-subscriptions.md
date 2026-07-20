# List Inactive Subscriptions with Steady

Retrieves inactive subscriptions for a Steady publication.

## Endpoint

- **Method:** `GET`
- **Path:** `/subscriptions/inactive`
- **Base URL:** `https://steadyhq.com/api/v1`
- **Official documentation:** [List Inactive Subscriptions](https://developers.steadyhq.com/#get-subscriptions-inactive)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[subscriber][email]` | query | `string` | no | A URL-encoded comma-separated list of subscriber email addresses to include. |
