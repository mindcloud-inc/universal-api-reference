# Claim Badge with Absinthe

Claims a badge for a user in Absinthe.

## Endpoint

- **Method:** `POST`
- **Path:** `/badges/{badge_id}/claim`
- **Base URL:** `https://api.absinthe.network`
- **Official documentation:** [Claim Badge](https://api.absinthe.network/doc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `badge_id` | path | `string` | no | UUID of the badge to claim. |
