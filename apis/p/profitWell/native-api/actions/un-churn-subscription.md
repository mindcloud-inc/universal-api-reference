# Un-Churn Subscription with ProfitWell

Reactivates a churned subscription in ProfitWell.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/unchurn/:subscriptionIdOrSubscriptionAlias/`
- **Base URL:** `https://api.profitwell.com`
- **Official documentation:** [Un-Churn Subscription](https://classic.paddle.com/profitwell/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriptionIdOrSubscriptionAlias` | path | `string` | yes | Either the subscription_id or the subscription_alias of the subscription you would like to un-churn. |
