# Delete management taxonomy group with Kontent.ai

Deletes a taxonomy group from Kontent.ai.

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://manage.kontent.ai/v2/projects/:environment_id/taxonomies/:taxonomy_group_identifier`
- **Base URL:** `https://deliver.kontent.ai`
- **Official documentation:** [Delete management taxonomy group](https://kontent.ai/learn/docs/apis/management-api-v2/taxonomy-groups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taxonomy_group_identifier` | path | `string` | yes | Kontent.ai taxonomy group identifier to delete. |
