# Retrieve taxonomy group with Kontent.ai

Retrieves a taxonomy group from Kontent.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/:environment_id/taxonomies/:taxonomy_group_codename`
- **Base URL:** `https://deliver.kontent.ai`
- **Official documentation:** [Retrieve taxonomy group](https://kontent.ai/learn/docs/apis/delivery-api/taxonomy-groups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environment_id` | path | `string` | yes | Kontent.ai project environment identifier. |
| `taxonomy_group_codename` | path | `string` | yes | Taxonomy group codename. |
