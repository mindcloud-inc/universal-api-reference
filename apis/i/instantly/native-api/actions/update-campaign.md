# Update Campaign with Instantly

Updates an existing campaign in Instantly.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/campaigns/:id`
- **Base URL:** `https://api.instantly.ai`
- **Official documentation:** [Update Campaign](https://developer.instantly.ai/api/v2/campaign/patchcampaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Campaign ID. |
| `name` | body | `string` | yes | Updated campaign name. |
