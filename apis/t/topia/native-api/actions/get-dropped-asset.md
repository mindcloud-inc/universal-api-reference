# Get Dropped Asset with Topia

Retrieves a dropped asset from a Topia world.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/world/:urlSlug/assets/:id`
- **Base URL:** `https://api.topia.io/api`
- **Official documentation:** [Get Dropped Asset](https://api.topia.io/api-docs/paths/v1/droppedAsset.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `urlSlug` | path | `string` | yes | Topia world URL slug. |
| `id` | path | `string` | yes | Identifier for the dropped asset. |
