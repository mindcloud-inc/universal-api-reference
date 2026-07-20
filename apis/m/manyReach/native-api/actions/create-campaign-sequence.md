# Create Campaign Sequence with ManyReach

Creates a sequence for a campaign in ManyReach.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.manyreach.com/api/v2/campaigns/:id/sequences`
- **Base URL:** `https://api.manyreach.com`
- **Official documentation:** [Create Campaign Sequence](https://api.manyreach.com/api#v2/tag/campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Campaign ID. |
| `name` | body | `string` | yes | Sequence name. |
