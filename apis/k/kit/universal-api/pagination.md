# Kit Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Kit expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kit/latest/actions/list-broadcasts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Kit actions that support pagination

- [List Broadcasts](actions/list-broadcasts.md)
- [List Custom Fields](actions/list-custom-fields.md)
- [List Form Subscribers](actions/list-form-subscribers.md)
- [List Forms](actions/list-forms.md)
- [List Segments](actions/list-segments.md)
- [List Sequence Subscribers](actions/list-sequence-subscribers.md)
- [List Sequences](actions/list-sequences.md)
- [List Subscribers](actions/list-subscribers.md)
- [List Tags](actions/list-tags.md)
- [List Tags for Subscriber](actions/list-tags-for-subscriber.md)
