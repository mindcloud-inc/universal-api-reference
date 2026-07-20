# Raisely Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Raisely expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/raisely/latest/actions/list-campaign-donations?connectionId=$CONNECTION_ID&limit=25&offset=0&campaign=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Raisely actions that support pagination

- [List Campaign Donations](actions/list-campaign-donations.md)
- [List Campaign Profiles](actions/list-campaign-profiles.md)
- [List Campaign Subscriptions](actions/list-campaign-subscriptions.md)
- [List Campaigns](actions/list-campaigns.md)
- [List Donations](actions/list-donations.md)
- [List Profile Members](actions/list-profile-members.md)
- [List Profiles](actions/list-profiles.md)
- [List Subscription Donations](actions/list-subscription-donations.md)
- [List Subscriptions](actions/list-subscriptions.md)
- [List Users](actions/list-users.md)
