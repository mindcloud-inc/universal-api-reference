# List items referencing item with Kontent.ai

Retrieves items referencing a content item in Kontent.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/:environment_id/items/:item_codename/used-in`
- **Base URL:** `https://deliver.kontent.ai`
- **Official documentation:** [List items referencing item](https://kontent.ai/learn/docs/apis/delivery-api/content-items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environment_id` | path | `string` | yes | Kontent.ai project environment identifier. |
| `item_codename` | path | `string` | yes | Content item codename to find inbound references for. |
