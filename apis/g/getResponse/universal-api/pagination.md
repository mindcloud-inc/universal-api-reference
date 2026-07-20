# GetResponse Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model GetResponse expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/get-account-login-history?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## GetResponse actions that support pagination

- [Get Account Login History](actions/get-account-login-history.md)
- [Get Newsletter Statistics](actions/get-newsletter-statistics.md)
- [List Addresses](actions/list-addresses.md)
- [List Campaigns](actions/list-campaigns.md)
- [List Contacts](actions/list-contacts.md)
- [List Custom Fields](actions/list-custom-fields.md)
- [List From Fields](actions/list-from-fields.md)
- [List Industries](actions/list-industries.md)
- [List Newsletters](actions/list-newsletters.md)
- [List Products](actions/list-products.md)
- [List Search Contacts](actions/list-search-contacts.md)
- [List Shops](actions/list-shops.md)
- [List Tags](actions/list-tags.md)
- [List Websites](actions/list-websites.md)
