# Churn Subscription with ProfitWell

Churns a subscription in ProfitWell.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v2/subscriptions/:subscriptionIdOrSubscriptionAlias/`
- **Base URL:** `https://api.profitwell.com`
- **Official documentation:** [Churn Subscription](https://classic.paddle.com/profitwell/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriptionIdOrSubscriptionAlias` | path | `string` | yes | Either the subscription_id or the subscription_alias of the subscription. |
| `effective_date` | query | `number` | yes | UNIX timestamp of when the subscription churns. |
| `churn_type` | query | `string` | no | Acceptable values are voluntary or delinquent. |
