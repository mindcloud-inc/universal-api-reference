# Google Cloud Pub/Sub Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Google Cloud Pub/Sub expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/list-schema-revisions?connectionId=$CONNECTION_ID&limit=25&offset=0&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Google Cloud Pub/Sub actions that support pagination

- [List Schema Revisions](actions/list-schema-revisions.md)
- [List Schemas](actions/list-schemas.md)
- [List Snapshots](actions/list-snapshots.md)
- [List Subscriptions](actions/list-subscriptions.md)
- [List Topic Snapshots](actions/list-topic-snapshots.md)
- [List Topic Subscriptions](actions/list-topic-subscriptions.md)
- [List Topics](actions/list-topics.md)
