# Delete management asset with Kontent.ai

Deletes an asset from your Kontent.ai environment.

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://manage.kontent.ai/v2/projects/:environment_id/assets/:asset_identifier`
- **Base URL:** `https://deliver.kontent.ai`
- **Official documentation:** [Delete management asset](https://kontent.ai/learn/docs/apis/management-api-v2/assets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `asset_identifier` | path | `string` | yes | Kontent.ai asset identifier for the asset to delete. |
