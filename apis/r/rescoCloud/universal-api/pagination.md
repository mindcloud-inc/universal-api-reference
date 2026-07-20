# Resco Cloud Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Resco Cloud expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rescoCloud/latest/actions/list-o-data-entity-records?connectionId=$CONNECTION_ID&limit=25&offset=0&entity=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Resco Cloud actions that support pagination

- [List OData Entity Records](actions/list-o-data-entity-records.md)
- [List Questionnaire Results](actions/list-questionnaire-results.md)
- [Select Records](actions/select-records.md)
