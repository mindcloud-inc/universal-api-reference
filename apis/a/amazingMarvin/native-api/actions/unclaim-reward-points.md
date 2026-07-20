# Unclaim Reward Points with Amazing Marvin

Unclaims reward points in Amazing Marvin.

## Endpoint

- **Method:** `POST`
- **Path:** `/unclaimRewardPoints`
- **Base URL:** `https://serv.amazingmarvin.com/api`
- **Official documentation:** [Unclaim Reward Points](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#unclaiming-reward-points)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `itemId` | body | `string` | yes | Which item or manual reward to undo. |
| `date` | body | `string` | yes | Date in YYYY-MM-DD format. |
