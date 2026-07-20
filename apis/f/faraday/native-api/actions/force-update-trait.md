# Force Update Trait with Faraday

Triggers a rerun for a trait in Faraday.

## Endpoint

- **Method:** `POST`
- **Path:** `/traits/:trait_id/force_update`
- **Base URL:** `https://api.faraday.ai/v1`
- **Official documentation:** [Force Update Trait](https://faraday.ai/docs/reference/forceupdatetrait)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `trait_id` | path | `string` | no | Faraday trait ID. |
