# Modify content type snippet with Kontent.ai

Modifies a content type snippet in Kontent.ai.

## Endpoint

- **Method:** `PATCH`
- **Path:** `https://manage.kontent.ai/v2/projects/:environment_id/snippets/:snippet_identifier`
- **Base URL:** `https://deliver.kontent.ai`
- **Official documentation:** [Modify content type snippet](https://kontent.ai/learn/docs/apis/management-api-v2/content-type-snippets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `snippet_identifier` | path | `string` | yes | Kontent.ai content type snippet identifier to modify. |
| `operations[]` | body | `array<object>` | yes | JSON Patch operations for modifying a Kontent.ai content type snippet. |
