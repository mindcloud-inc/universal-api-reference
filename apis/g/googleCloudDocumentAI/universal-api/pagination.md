# Google Cloud Document AI Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Google Cloud Document AI expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleCloudDocumentAI/latest/actions/list-location-operations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Google Cloud Document AI actions that support pagination

- [List Location Operations](actions/list-location-operations.md)
- [List Locations](actions/list-locations.md)
- [List Processor Types](actions/list-processor-types.md)
- [List Processor Version Evaluations](actions/list-processor-version-evaluations.md)
- [List Processor Versions](actions/list-processor-versions.md)
- [List Processors](actions/list-processors.md)
- [List Schema Versions](actions/list-schema-versions.md)
- [List Schemas](actions/list-schemas.md)
