# Revert a feature to a specific revision with GrowthBook

Reverts a feature to a specific GrowthBook revision.

## Endpoint

- **Method:** `POST`
- **Path:** `/features/:id/revert`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Revert a feature to a specific revision](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The id of the requested resource |
| `revision` | body | `number` | yes | — |
| `comment` | body | `string` | no | — |
