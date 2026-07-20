# PromptLayer Run Agent Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model PromptLayer Run Agent expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/get-dataset-rows?connectionId=$CONNECTION_ID&limit=25&offset=0&datasetId=32101" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## PromptLayer Run Agent actions that support pagination

- [Get Dataset Rows](actions/get-dataset-rows.md)
- [Get Evaluation Rows](actions/get-evaluation-rows.md)
- [List Agents](actions/list-agents.md)
- [List Datasets](actions/list-datasets.md)
- [List Evaluations](actions/list-evaluations.md)
- [List Prompt Templates](actions/list-prompt-templates.md)
