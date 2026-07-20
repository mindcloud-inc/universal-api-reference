# Update Reward with GoAffPro

Updates an existing reward in GoAffPro.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/admin/rewards/:id`
- **Base URL:** `https://api.goaffpro.com/v1`
- **Official documentation:** [Update Reward](https://api.goaffpro.com/docs/admin/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Reward ID. |
| `status` | body | `string` | no | Reward status. |
| `amount` | body | `number` | no | Reward amount. |
