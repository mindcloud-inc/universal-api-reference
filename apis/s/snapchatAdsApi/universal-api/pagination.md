# Snapchat Ads Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Snapchat Ads expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/list-ad-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Snapchat Ads actions that support pagination

- [List Ad Accounts](actions/list-ad-accounts.md)
- [List Ad Squads by Ad Account](actions/list-ad-squads-by-ad-account.md)
- [List Ad Squads by Campaign](actions/list-ad-squads-by-campaign.md)
- [List Ads by Ad Account](actions/list-ads-by-ad-account.md)
- [List Ads by Ad Squad](actions/list-ads-by-ad-squad.md)
- [List Ads by Campaign](actions/list-ads-by-campaign.md)
- [List Billing Centers](actions/list-billing-centers.md)
- [List Campaigns](actions/list-campaigns.md)
- [List Creatives](actions/list-creatives.md)
- [List Media](actions/list-media.md)
