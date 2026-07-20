# Update Reward with Vouchery.io

## Endpoint

- **Method:** `PUT`
- **Path:** `/rewards/:id`
- **Base URL:** `https://mindcloud.sandbox.vouchery.app/api/v2.1`
- **Official documentation:** [Update Reward](https://docs.vouchery.io/reference/putapiv21rewardsid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | yes | Updated reward description. |
| `id` | path | `number` | yes | Reward ID from Vouchery. |
| `title` | body | `string` | yes | Updated reward title. |
| `type` | body | `string` | yes | Reward type discriminator for update. |
| `value` | body | `number` | yes | Updated reward value. |
