# Delete content type snippet with Kontent.ai

Deletes a content type snippet from Kontent.ai.

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://manage.kontent.ai/v2/projects/:environment_id/snippets/:snippet_identifier`
- **Base URL:** `https://deliver.kontent.ai`
- **Official documentation:** [Delete content type snippet](https://kontent.ai/learn/docs/apis/management-api-v2/content-type-snippets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `snippet_identifier` | path | `string` | yes | Kontent.ai content type snippet identifier to delete. |
