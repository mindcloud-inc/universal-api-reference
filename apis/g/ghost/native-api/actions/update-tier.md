# Update Tier with Ghost

Updates an existing tier in Ghost.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tiers/:id/`
- **Base URL:** `{adminDomain}/ghost/api/admin`
- **Official documentation:** [Update Tier](https://docs.ghost.org/admin-api/tiers/updating-a-tier)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Ghost tier ID from the URL path. |
| `tiers[0].name` | body | `string` | no | Updated tier name. |
| `tiers[0].description` | body | `string` | no | Updated public description for the tier. |
| `tiers[0].active` | body | `boolean` | no | Whether the tier should remain active. |
