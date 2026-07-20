# List Dropped Assets with Topia

Retrieves dropped assets from a Topia world.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/world/:urlSlug/assets`
- **Base URL:** `https://api.topia.io/api`
- **Official documentation:** [List Dropped Assets](https://api.topia.io/api-docs/paths/v1/droppedAssets.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `urlSlug` | path | `string` | yes | The Topia world slug. |
