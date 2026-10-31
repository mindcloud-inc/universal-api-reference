# Bridgit Bench Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Bridgit Bench expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/get-account-integration?connectionId=$CONNECTION_ID&limit=25&offset=0&accountId=1&view=All" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Bridgit Bench actions that support pagination

- [Get Account Integration](actions/get-account-integration.md)
- [Get Workforce Spend Hours Breakdown](actions/get-workforce-spend-hours-breakdown.md)
- [Get Workforce Spend Hours Overview](actions/get-workforce-spend-hours-overview.md)
- [List Account Certifications](actions/list-account-certifications.md)
- [List Account Groupings](actions/list-account-groupings.md)
- [List Account Hourly Roles](actions/list-account-hourly-roles.md)
- [List Account Invitations](actions/list-account-invitations.md)
- [List Account Person Certifications](actions/list-account-person-certifications.md)
- [List Account Person Field Values](actions/list-account-person-field-values.md)
- [List Account Project Field Values](actions/list-account-project-field-values.md)
- [List Account Role Categories](actions/list-account-role-categories.md)
- [List Account Salaried Roles](actions/list-account-salaried-roles.md)
- [List Account Tasks](actions/list-account-tasks.md)
- [List Account User Profiles](actions/list-account-user-profiles.md)
- [List Account Users](actions/list-account-users.md)
- [List Accounts](actions/list-accounts.md)
- [List Experience Field Values](actions/list-experience-field-values.md)
- [List Hourly Allocations](actions/list-hourly-allocations.md)
- [List People](actions/list-people.md)
- [List Person Attachments](actions/list-person-attachments.md)
- [List Person Certification Attachments](actions/list-person-certification-attachments.md)
- [List Person Certifications](actions/list-person-certifications.md)
- [List Person Historical Experiences](actions/list-person-historical-experiences.md)
- [List Person Unavailabilities](actions/list-person-unavailabilities.md)
- [List Project Allocations](actions/list-project-allocations.md)
- [List Project Notes](actions/list-project-notes.md)
- [List Projects](actions/list-projects.md)
- [List Saved Filters](actions/list-saved-filters.md)
- [Search Account Activities](actions/search-account-activities.md)
- [Search Accounts](actions/search-accounts.md)
- [Search People](actions/search-people.md)
- [Search Person Collaborations](actions/search-person-collaborations.md)
- [Search Projects](actions/search-projects.md)
