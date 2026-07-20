# InsightIQ Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model InsightIQ expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/get-trending-creators?connectionId=$CONNECTION_ID&limit=25&offset=0&workPlatformId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## InsightIQ actions that support pagination

- [Get Trending Creators](actions/get-trending-creators.md)
- [Get Trending Hashtags](actions/get-trending-hashtags.md)
- [Get Trending Videos](actions/get-trending-videos.md)
- [List Creator Locations](actions/list-creator-locations.md)
- [List Flagging Criteria](actions/list-flagging-criteria.md)
- [List Professional Companies](actions/list-professional-companies.md)
- [List Professional Education Degrees](actions/list-professional-education-degrees.md)
- [List Professional Education Institutes](actions/list-professional-education-institutes.md)
- [List Professional Locations](actions/list-professional-locations.md)
- [List Professional Talks About](actions/list-professional-talks-about.md)
- [List Professional Topics](actions/list-professional-topics.md)
- [List Users](actions/list-users.md)
- [List Webhooks](actions/list-webhooks.md)
- [List Work Platforms](actions/list-work-platforms.md)
