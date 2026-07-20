# Search Issued Rewards with Referral Factory

Finds issued rewards in Referral Factory by metric.

## Endpoint

- **Method:** `POST`
- **Path:** `/rewards/issued/:metric/search`
- **Base URL:** `https://referral-factory.com/api/v2`
- **Official documentation:** [Search Issued Rewards](https://developers.referral-factory.com/reference/search-rewards-issued)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `metric` | path | `string` | yes | Issued reward dashboard metric to search. |
