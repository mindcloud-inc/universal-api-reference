# HubSpot Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model HubSpot expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/list-associations?connectionId=$CONNECTION_ID&limit=25&offset=0&fromObject=string&objectId=string&toObjectType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## HubSpot actions that support pagination

- [List Associations](actions/list-associations.md)
- [List Companies](actions/list-companies.md)
- [List Contacts](actions/list-contacts.md)
- [List Deals](actions/list-deals.md)
- [List Emails](actions/list-emails.md)
- [List Owners](actions/list-owners.md)
- [List Subscriptions](actions/list-subscriptions.md)
- [List Tickets](actions/list-tickets.md)
- [List Users](actions/list-users.md)
- [Search Companies](actions/search-companies.md)
- [Search Contacts](actions/search-contacts.md)
- [Search Deals](actions/search-deals.md)
- [Search Subscriptions](actions/search-subscriptions.md)
- [Search Tickets](actions/search-tickets.md)
