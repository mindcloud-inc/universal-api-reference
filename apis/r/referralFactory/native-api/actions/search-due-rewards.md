# Search Due Rewards with Referral Factory

Finds due rewards in Referral Factory by metric.

## Endpoint

- **Method:** `POST`
- **Path:** `/rewards/due/:metric/search`
- **Base URL:** `https://referral-factory.com/api/v2`
- **Official documentation:** [Search Due Rewards](https://developers.referral-factory.com/reference/search-rewards-due)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `metric` | path | `string` | yes | Due reward dashboard metric to search. |
