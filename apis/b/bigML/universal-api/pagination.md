# BigML Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model BigML expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigML/latest/actions/list-anomalies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## BigML actions that support pagination

- [List Anomalies](actions/list-anomalies.md)
- [List Batch Predictions](actions/list-batch-predictions.md)
- [List Clusters](actions/list-clusters.md)
- [List Datasets](actions/list-datasets.md)
- [List Ensembles](actions/list-ensembles.md)
- [List Evaluations](actions/list-evaluations.md)
- [List Models](actions/list-models.md)
- [List Predictions](actions/list-predictions.md)
- [List Projects](actions/list-projects.md)
- [List Sources](actions/list-sources.md)
