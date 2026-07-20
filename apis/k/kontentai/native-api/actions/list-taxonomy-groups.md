# List taxonomy groups with Kontent.ai

Retrieves taxonomy groups from your Kontent.ai environment.

## Endpoint

- **Method:** `GET`
- **Path:** `/:environment_id/taxonomies`
- **Base URL:** `https://deliver.kontent.ai`
- **Official documentation:** [List taxonomy groups](https://kontent.ai/learn/docs/apis/delivery-api/taxonomy-groups)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environment_id` | path | `string` | yes | Kontent.ai project environment identifier. |
