# List Due Rewards with Referral Factory

Retrieves due rewards from Referral Factory by metric.

## Endpoint

- **Method:** `GET`
- **Path:** `/rewards/due/:metric`
- **Base URL:** `https://referral-factory.com/api/v2`
- **Official documentation:** [List Due Rewards](https://developers.referral-factory.com/reference/list-all-due-rewards)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `metric` | path | `string` | yes | Due reward dashboard metric to retrieve. |
