# List content types with Kontent.ai

Retrieves content types from your Kontent.ai environment.

## Endpoint

- **Method:** `GET`
- **Path:** `/:environment_id/types`
- **Base URL:** `https://deliver.kontent.ai`
- **Official documentation:** [List content types](https://kontent.ai/learn/docs/apis/delivery-api/content-types)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environment_id` | path | `string` | yes | Kontent.ai project environment identifier. |
