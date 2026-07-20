# List Dropped Assets by Scene Drop ID with Topia

Retrieves dropped assets in Topia by scene drop ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/world/:urlSlug/assets-with-scene-drop-id/:sceneDropId`
- **Base URL:** `https://api.topia.io/api`
- **Official documentation:** [List Dropped Assets by Scene Drop ID](https://api.topia.io/api-docs/paths/v1/droppedAssetsBySceneDropId.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `urlSlug` | path | `string` | yes | Topia world URL slug. |
| `sceneDropId` | path | `string` | yes | Identifier for the scene drop. |
