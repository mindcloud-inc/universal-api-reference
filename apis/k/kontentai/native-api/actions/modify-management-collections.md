# Modify management collections with Kontent.ai

Modifies collections in your Kontent.ai environment.

## Endpoint

- **Method:** `PATCH`
- **Path:** `https://manage.kontent.ai/v2/projects/:environment_id/collections`
- **Base URL:** `https://deliver.kontent.ai`
- **Official documentation:** [Modify management collections](https://kontent.ai/learn/docs/apis/management-api-v2/collections)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `operations[]` | body | `array<object>` | yes | JSON Patch operations for modifying Kontent.ai collections. |
