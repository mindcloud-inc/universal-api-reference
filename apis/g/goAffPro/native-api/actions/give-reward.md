# Give Reward with GoAffPro

Creates a reward for an affiliate in GoAffPro.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/rewards`
- **Base URL:** `https://api.goaffpro.com/v1`
- **Official documentation:** [Give Reward](https://api.goaffpro.com/docs/admin/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rewards[]` | body | `array<object>` | yes | Rewards to give to affiliates. |
