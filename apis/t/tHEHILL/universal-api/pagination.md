# THE HILL Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model THE HILL expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tHEHILL/latest/actions/list-alerts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## THE HILL actions that support pagination

- [List Alerts](actions/list-alerts.md)
- [List Categories](actions/list-categories.md)
- [List City Tags](actions/list-city-tags.md)
- [List Company Tags](actions/list-company-tags.md)
- [List Country Tags](actions/list-country-tags.md)
- [List Email Newsletters](actions/list-email-newsletters.md)
- [List Events](actions/list-events.md)
- [List Events Facts Tags](actions/list-events-facts-tags.md)
- [List Feed Posts](actions/list-feed-posts.md)
- [List Future America Posts](actions/list-future-america-posts.md)
- [List Galleries](actions/list-galleries.md)
- [List HillTV Posts](actions/list-hilltv-posts.md)
- [List Link Posts](actions/list-link-posts.md)
- [List Media](actions/list-media.md)
- [List Navigation](actions/list-navigation.md)
- [List Newsletter Posts](actions/list-newsletter-posts.md)
- [List Nota](actions/list-nota.md)
- [List Pages](actions/list-pages.md)
- [List Posts](actions/list-posts.md)
- [List Statuses](actions/list-statuses.md)
- [List Tags](actions/list-tags.md)
- [List Vertical Posts](actions/list-vertical-posts.md)
- [List Videos](actions/list-videos.md)
- [Search Content](actions/search-content.md)
