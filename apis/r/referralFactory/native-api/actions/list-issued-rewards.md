# List Issued Rewards with Referral Factory

Retrieves issued rewards from Referral Factory by metric.

## Endpoint

- **Method:** `GET`
- **Path:** `/rewards/issued/:metric`
- **Base URL:** `https://referral-factory.com/api/v2`
- **Official documentation:** [List Issued Rewards](https://developers.referral-factory.com/reference/list-all-issued-rewards)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `metric` | path | `string` | yes | Issued reward dashboard metric to retrieve. |
