# StoryChief Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model StoryChief expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/storyChief/latest/actions/list-authors?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## StoryChief actions that support pagination

- [List Authors](actions/list-authors.md)
- [List Categories](actions/list-categories.md)
- [List Contact Lists](actions/list-contact-lists.md)
- [List Contacts](actions/list-contacts.md)
- [List Destinations](actions/list-destinations.md)
- [List Posts](actions/list-posts.md)
- [List Stories](actions/list-stories.md)
- [List Tags](actions/list-tags.md)
- [List Users](actions/list-users.md)
