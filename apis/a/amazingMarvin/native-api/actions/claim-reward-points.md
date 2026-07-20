# Claim Reward Points with Amazing Marvin

Claims reward points in Amazing Marvin.

## Endpoint

- **Method:** `POST`
- **Path:** `/claimRewardPoints`
- **Base URL:** `https://serv.amazingmarvin.com/api`
- **Official documentation:** [Claim Reward Points](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#claiming-reward-points)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `points` | body | `number` | yes | Number of reward points. |
| `itemId` | body | `string` | yes | Task ID or MANUAL for a manual reward. |
| `date` | body | `string` | yes | Date in YYYY-MM-DD format. |
