# Spend Reward Points with Amazing Marvin

Spends reward points in Amazing Marvin.

## Endpoint

- **Method:** `POST`
- **Path:** `/spendRewardPoints`
- **Base URL:** `https://serv.amazingmarvin.com/api`
- **Official documentation:** [Spend Reward Points](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#spending-reward-points)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `points` | body | `number` | yes | Number of reward points to spend. |
| `date` | body | `string` | yes | Date in YYYY-MM-DD format. |
