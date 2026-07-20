# Reddit Lead Ads Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Reddit Lead Ads expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/get-a-report?connectionId=$CONNECTION_ID&limit=25&offset=0&adAccountId=string&data=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Reddit Lead Ads actions that support pagination

- [Get A Report](actions/get-a-report.md)
- [Get Ad Account History](actions/get-ad-account-history.md)
- [List Ad Accounts By Business](actions/list-ad-accounts-by-business.md)
- [List Ad Groups](actions/list-ad-groups.md)
- [List Ads](actions/list-ads.md)
- [List Campaigns](actions/list-campaigns.md)
- [List Devices](actions/list-devices.md)
- [List Lead Gen Forms](actions/list-lead-gen-forms.md)
- [List My Businesses](actions/list-my-businesses.md)
- [List Pixels By Ad Account](actions/list-pixels-by-ad-account.md)
- [List Pixels By Business](actions/list-pixels-by-business.md)
- [List Saved Audiences](actions/list-saved-audiences.md)
- [List User Custom Audiences](actions/list-user-custom-audiences.md)
- [Query Ad Accounts](actions/query-ad-accounts.md)
- [Search Communities](actions/search-communities.md)
