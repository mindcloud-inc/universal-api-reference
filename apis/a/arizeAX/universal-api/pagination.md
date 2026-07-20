# Arize AX Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Arize AX expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/arizeAX/latest/actions/list-datasets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Arize AX actions that support pagination

- [List Datasets](actions/list-datasets.md)
- [List Evaluator Versions](actions/list-evaluator-versions.md)
- [List Evaluators](actions/list-evaluators.md)
- [List Experiments](actions/list-experiments.md)
- [List Projects](actions/list-projects.md)
- [List Prompt Versions](actions/list-prompt-versions.md)
- [List Prompts](actions/list-prompts.md)
- [List Spaces](actions/list-spaces.md)
- [List Spans](actions/list-spans.md)
