# Centerpoint Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Centerpoint expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-companies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Centerpoint actions that support pagination

- [List Companies](actions/list-companies.md)
- [List Contacts](actions/list-contacts.md)
- [List Model Files](actions/list-model-files.md)
- [List Opportunities](actions/list-opportunities.md)
- [List Productions](actions/list-productions.md)
- [List Productions_items](actions/list-productions-items.md)
- [List Productions With Domain Production Only](actions/list-productions-with-domain-production-only.md)
- [List Properties](actions/list-properties.md)
- [List Services](actions/list-services.md)
