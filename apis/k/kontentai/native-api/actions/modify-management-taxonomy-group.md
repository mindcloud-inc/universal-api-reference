# Modify management taxonomy group with Kontent.ai

Modifies a taxonomy group in Kontent.ai.

## Endpoint

- **Method:** `PATCH`
- **Path:** `https://manage.kontent.ai/v2/projects/:environment_id/taxonomies/:taxonomy_group_identifier`
- **Base URL:** `https://deliver.kontent.ai`
- **Official documentation:** [Modify management taxonomy group](https://kontent.ai/learn/docs/apis/management-api-v2/taxonomy-groups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taxonomy_group_identifier` | path | `string` | yes | Kontent.ai taxonomy group identifier to modify. |
| `operations[]` | body | `array<object>` | yes | JSON Patch operations for modifying a Kontent.ai taxonomy group. |
