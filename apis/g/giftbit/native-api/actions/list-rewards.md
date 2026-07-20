# List Rewards with Giftbit

Lists rewards in your Giftbit account.

## Endpoint

- **Method:** `GET`
- **Path:** `/gifts`
- **Base URL:** `https://api-testbed.giftbit.com/papi/v1`
- **Official documentation:** [List Rewards](https://www.giftbit.com/api-documentation)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `uuid` | query | `string` | no |
| `campaign_uuid` | query | `string` | no |
| `campaign_id` | query | `string` | no |
| `recipient_name` | query | `string` | no |
| `recipient_email` | query | `string` | no |
| `delivery_status` | query | `string` | no |
| `status` | query | `string` | no |
| `price_in_cents_greater_than` | query | `number` | no |
| `price_in_cents_less_than` | query | `number` | no |
| `created_date_greater_than` | query | `date` | no |
| `created_date_less_than` | query | `date` | no |
| `delivery_date_greater_than` | query | `date` | no |
| `delivery_date_less_than` | query | `date` | no |
| `redeemed_date_greater_than` | query | `date` | no |
| `redeemed_date_less_than` | query | `date` | no |
| `redelivery_count_greater_than` | query | `number` | no |
| `redelivery_count_less_than` | query | `number` | no |
| `sort` | query | `string` | no |
| `order` | query | `string` | no |
