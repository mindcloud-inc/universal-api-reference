# Zoho Meeting Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Zoho Meeting expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/list-meetings?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationId=%7B%7Bcredentials.organizationId%7D%7D&listType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Zoho Meeting actions that support pagination

- [List Meetings](actions/list-meetings.md)
- [List Users](actions/list-users.md)
- [List Webinar Registrations](actions/list-webinar-registrations.md)
- [List Webinars](actions/list-webinars.md)
