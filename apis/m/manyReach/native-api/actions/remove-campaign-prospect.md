# Remove Campaign Prospect with ManyReach

Deletes a prospect from a campaign in ManyReach.

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://api.manyreach.com/api/v2/campaigns/:id/prospects/:prospectId`
- **Base URL:** `https://api.manyreach.com`
- **Official documentation:** [Remove Campaign Prospect](https://api.manyreach.com/api#v2/tag/campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Campaign ID. |
| `prospectId` | path | `string` | no | Prospect ID. |
