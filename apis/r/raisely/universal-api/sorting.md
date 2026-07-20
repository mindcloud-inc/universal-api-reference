# Raisely Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Raisely expects, and each action page lists the fields available to sort.

## Raisely actions that support sorting

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
