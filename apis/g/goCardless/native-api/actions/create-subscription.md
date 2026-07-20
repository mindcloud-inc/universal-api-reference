# Create Subscription with GoCardless

Creates a new subscription in GoCardless.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscriptions`
- **Base URL:** `https://api-sandbox.gocardless.com`
- **Official documentation:** [Create Subscription](https://developer.gocardless.com/api-reference/#subscriptions-create-a-subscription)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `amount` | body | `number` | yes |
| `currency` | body | `string` | yes |
| `interval_unit` | body | `string` | yes |
| `links[mandate]` | body | `string` | yes |
| `interval` | body | `number` | no |
| `day_of_month` | body | `number` | no |
| `month` | body | `string` | no |
| `start_date` | body | `date` | no |
| `count` | body | `number` | no |
| `end_date` | body | `date` | no |
| `name` | body | `string` | no |
| `payment_reference` | body | `string` | no |
| `app_fee` | body | `number` | no |
| `retry_if_possible` | body | `boolean` | no |
| `metadata` | body | `object` | no |
