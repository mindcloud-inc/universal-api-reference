# List languages with Kontent.ai

Retrieves languages from your Kontent.ai environment.

## Endpoint

- **Method:** `GET`
- **Path:** `/:environment_id/languages`
- **Base URL:** `https://deliver.kontent.ai`
- **Official documentation:** [List languages](https://kontent.ai/learn/docs/apis/delivery-api/languages)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environment_id` | path | `string` | yes | Kontent.ai project environment identifier. |
