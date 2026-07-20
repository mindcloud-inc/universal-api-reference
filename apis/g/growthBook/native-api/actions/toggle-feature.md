# Toggle a feature in one or more environments with GrowthBook

Toggles a feature in GrowthBook environments.

## Endpoint

- **Method:** `POST`
- **Path:** `/features/:id/toggle`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Toggle a feature in one or more environments](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The id of the requested resource |
| `reason` | body | `string` | no | — |
| `environments` | body | `object` | yes | — |
