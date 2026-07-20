# Clarifai Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Clarifai expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/list-apps?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Clarifai actions that support pagination

- [List Apps](actions/list-apps.md)
- [List Concepts](actions/list-concepts.md)
- [List Dataset Versions](actions/list-dataset-versions.md)
- [List Datasets](actions/list-datasets.md)
- [List Inputs](actions/list-inputs.md)
- [List Model Concepts](actions/list-model-concepts.md)
- [List Model Versions](actions/list-model-versions.md)
- [List Models](actions/list-models.md)
- [List Public Models](actions/list-public-models.md)
- [List Workflows](actions/list-workflows.md)
