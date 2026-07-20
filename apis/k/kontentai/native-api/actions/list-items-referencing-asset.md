# List items referencing asset with Kontent.ai

Retrieves items referencing an asset in Kontent.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/:environment_id/assets/:asset_id/used-in`
- **Base URL:** `https://deliver.kontent.ai`
- **Official documentation:** [List items referencing asset](https://kontent.ai/learn/docs/apis/delivery-api/content-items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environment_id` | path | `string` | yes | Kontent.ai project environment identifier. |
| `asset_id` | path | `string` | yes | Asset ID to find inbound references for. |
