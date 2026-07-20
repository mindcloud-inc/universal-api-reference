# Get Dropped Asset by Unique Name with Topia

Finds a dropped asset in Topia by unique name.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/world/:urlSlug/asset-by-unique-name/:uniqueName`
- **Base URL:** `https://api.topia.io/api`
- **Official documentation:** [Get Dropped Asset by Unique Name](https://api.topia.io/api-docs/paths/v1/droppedAssetByUniqueName.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `urlSlug` | path | `string` | yes | Topia world URL slug. |
| `uniqueName` | path | `string` | yes | Unique name assigned to the dropped asset. |
