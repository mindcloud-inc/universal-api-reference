# Upgrade Or Downgrade Subscription with ProfitWell

Updates a subscription in ProfitWell.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/subscriptions/:subscriptionIdOrSubscriptionAlias/`
- **Base URL:** `https://api.profitwell.com`
- **Official documentation:** [Upgrade Or Downgrade Subscription](https://classic.paddle.com/profitwell/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriptionIdOrSubscriptionAlias` | path | `string` | yes | Either the subscription_id or the subscription_alias of the subscription. |
| `effective_date` | body | `number` | yes | The date that this update takes effect, in UNIX timestamp format. |
| `plan_id` | body | `string` | yes | The ID of the plan that the user is switching to. |
| `plan_interval` | body | `string` | yes | The billing cycle for this plan. The two options are month and year. |
| `status` | body | `string` | no | The only valid status when upgrading or downgrading a subscription is active. |
| `value` | body | `number` | yes | The new amount that you bill your user, per billing period, in cents. |
