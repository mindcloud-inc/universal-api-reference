# Zoho CRM Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Zoho CRM expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/get-notes-for-record?connectionId=$CONNECTION_ID&limit=25&offset=0&moduleApiName=Leads&recordId=7323083000000731821&fields=Owner%2CParent_Id%2CNote_Title%2CNote_Content%2CCreated_Time" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Zoho CRM actions that support pagination

- [Get Notes for Record](actions/get-notes-for-record.md)
- [Get Related Records](actions/get-related-records.md)
- [Get Users](actions/get-users.md)
- [List Contacts](actions/list-contacts.md)
- [List Deals](actions/list-deals.md)
- [List Leads](actions/list-leads.md)
- [Search Accounts](actions/search-accounts.md)
- [Search Contacts](actions/search-contacts.md)
- [Search Deals](actions/search-deals.md)
- [Search Leads](actions/search-leads.md)
- [Search Opportunity Groups](actions/search-opportunity-groups.md)
