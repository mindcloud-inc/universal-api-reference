# BHuman Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model BHuman expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bHuman/latest/actions/list-generated-videos-by-campaign?connectionId=$CONNECTION_ID&limit=25&offset=0&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## BHuman actions that support pagination

- [List Generated Videos by Campaign](actions/list-generated-videos-by-campaign.md)
- [List Generated Videos by Instance](actions/list-generated-videos-by-instance.md)
- [List Video Instances](actions/list-video-instances.md)
