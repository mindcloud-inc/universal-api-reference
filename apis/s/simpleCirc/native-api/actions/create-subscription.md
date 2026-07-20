# Create Subscription with SimpleCirc

Creates a subscription in SimpleCirc, or renews an existing one.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1.2/subscribers/:account_id/subscriptions`
- **Base URL:** `https://simplecirc.com`
- **Official documentation:** [Create Subscription](https://simplecirc.com/docs/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `publication_id` | body | `number` | yes |
| `issues_purchased` | body | `number` | yes |
| `copies` | body | `number` | no |
| `postage_id` | body | `number` | no |
| `promo_code` | body | `string` | no |
| `giftgiver_account_id` | body | `string` | no |
| `never_expires` | body | `boolean` | no |
| `qualified` | body | `boolean` | no |
| `qualified_on` | body | `date` | no |
| `do_not_renew` | body | `boolean` | no |
| `amount_paid` | body | `number` | no |
| `amount_due` | body | `number` | no |
| `tax_amount` | body | `number` | no |
| `currency` | body | `string` | no |
| `questions` | body | `object` | no |
