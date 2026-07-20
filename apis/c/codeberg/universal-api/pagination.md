# Codeberg Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Codeberg expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-blocked-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Codeberg actions that support pagination

- [List Blocked Users](actions/list-blocked-users.md)
- [List Current User Followers](actions/list-current-user-followers.md)
- [List Current User Following](actions/list-current-user-following.md)
- [List Current User GPG Keys](actions/list-current-user-gpg-keys.md)
- [List Current User Organizations](actions/list-current-user-organizations.md)
- [List Current User Public Keys](actions/list-current-user-public-keys.md)
- [List Current User Quota Artifacts](actions/list-current-user-quota-artifacts.md)
- [List Current User Quota Attachments](actions/list-current-user-quota-attachments.md)
- [List Current User Quota Packages](actions/list-current-user-quota-packages.md)
- [List Current User Repositories](actions/list-current-user-repositories.md)
- [List Current User Webhooks](actions/list-current-user-webhooks.md)
- [List Notifications](actions/list-notifications.md)
- [List Organizations](actions/list-organizations.md)
- [List Starred Repositories](actions/list-starred-repositories.md)
- [List Stopwatches](actions/list-stopwatches.md)
- [List User Actions Variables](actions/list-user-actions-variables.md)
- [List User OAuth2 Applications](actions/list-user-oauth2-applications.md)
- [List User Teams](actions/list-user-teams.md)
- [List User Tracked Times](actions/list-user-tracked-times.md)
- [List Watched Repositories](actions/list-watched-repositories.md)
- [Search Issues](actions/search-issues.md)
- [Search Repositories](actions/search-repositories.md)
- [Search Users](actions/search-users.md)
