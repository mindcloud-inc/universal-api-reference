# List Subscribers with PayWhirl

Retrieves subscribers from PayWhirl.

## Endpoint

- **Method:** `GET`
- **Path:** `/subscribers`
- **Base URL:** `https://api.paywhirl.com`
- **Official documentation:** [List Subscribers](https://api.paywhirl.com/#subscriptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keyword` | query | `string` | no | Optional keyword filter. |
| `limit` | query | `number` | no | Number of subscriber records to return. |
| `order` | query | `string` | no | Overall result order. Use asc, desc, or rand. |
| `order_direction` | query | `string` | no | Sort direction. Use asc or desc. |
| `order_key` | query | `string` | no | Subscriber field to sort by. |
| `starting_after` | query | `number` | no | Return subscribers with subscription IDs greater than this value. |
| `starting_before` | query | `number` | no | Return subscribers with subscription IDs lower than this value. |
