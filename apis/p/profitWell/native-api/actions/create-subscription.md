# Create Subscription with ProfitWell

Creates a subscription in ProfitWell.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/subscriptions/`
- **Base URL:** `https://api.profitwell.com`
- **Official documentation:** [Create Subscription](https://classic.paddle.com/profitwell/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_alias` | body | `string` | no | Your own identifier for this user so that you have a handle by which to refer to this user in subsequent requests. |
| `subscription_alias` | body | `string` | no | Your own identifier for this subscription. Must be unique across all users in your company. Maximum length: 36. |
| `email` | body | `string` | yes | The email address of the user. |
| `plan_id` | body | `string` | yes | The ID of the plan that the user is on. |
| `plan_interval` | body | `string` | yes | The billing cycle for this plan. The two options are month and year. |
| `plan_currency` | body | `string` | no | The currency in which users of this plan are charged. |
| `status` | body | `string` | no | The status of the subscription. Acceptable values for new subscriptions are active and trialing. |
| `value` | body | `number` | yes | The amount that you bill your user, per billing period, in cents. |
| `effective_date` | body | `number` | yes | The date that the subscription starts, in UNIX timestamp format. |
