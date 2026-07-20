# Odoo Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Odoo expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/odoo/latest/actions/list-access-controls?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Odoo actions that support pagination

- [List Access Controls](actions/list-access-controls.md)
- [List Access Rules](actions/list-access-rules.md)
- [List Departments](actions/list-accounts.md)
- [List Action Windows](actions/list-action-windows.md)
- [List Activities](actions/list-activities.md)
- [List Activity Types](actions/list-activity-types.md)
- [List Bank Accounts](actions/list-bank-accounts.md)
- [List Blacklisted Emails](actions/list-blacklisted-emails.md)
- [List Blacklisted Phone Numbers](actions/list-blacklisted-phone-numbers.md)
- [List System Parameters](actions/list-campaigns.md)
- [List Channel Members](actions/list-channel-members.md)
- [List Companies](actions/list-companies.md)
- [List Contact Tags](actions/list-contact-tags.md)
- [List Contacts](actions/list-contacts.md)
- [List Contract Types](actions/list-contract-types.md)
- [List Countries](actions/list-countries.md)
- [List Country Groups](actions/list-country-groups.md)
- [List Country States](actions/list-country-states.md)
- [List Currency Rates](actions/list-currency-rates.md)
- [List Departure Reasons](actions/list-departure-reasons.md)
- [List Discussion Categories](actions/list-discussion-categories.md)
- [List Discussion Channels](actions/list-discussion-channels.md)
- [List Email Aliases](actions/list-email-aliases.md)
- [List Email Domains](actions/list-email-domains.md)
- [List Email Templates](actions/list-email-templates.md)
- [List Employee Categories](actions/list-employee-categories.md)
- [List Employee Locations](actions/list-employee-locations.md)
- [List Employee Skills](actions/list-employee-skills.md)
- [List Employees](actions/list-employees.md)
- [List Field Selections](actions/list-field-selections.md)
- [List Job Positions](actions/list-job-positions.md)
- [List Attachments](actions/list-journal-entries.md)
- [List Messages](actions/list-journal-entry-lines.md)
- [List Scheduled Actions](actions/list-leads.md)
- [List Logs](actions/list-logs.md)
- [List Mail Servers](actions/list-mail-servers.md)
- [List Message Notifications](actions/list-message-notifications.md)
- [List Message Subtypes](actions/list-message-subtypes.md)
- [List Model Constraints](actions/list-model-constraints.md)
- [List Module Categories](actions/list-module-categories.md)
- [List Models](actions/list-payment-terms.md)
- [List Planning Roles](actions/list-planning-roles.md)
- [List Planning Shifts](actions/list-planning-shifts.md)
- [List Views](actions/list-pricelists.md)
- [List Model Data](actions/list-product-categories.md)
- [List Modules](actions/list-product-templates.md)
- [List Model Fields](actions/list-products.md)
- [List Industries](actions/list-purchase-order-lines.md)
- [List Groups](actions/list-purchase-orders.md)
- [List Resource Calendars](actions/list-resource-calendars.md)
- [List Resume Line Types](actions/list-resume-line-types.md)
- [List Resume Lines](actions/list-resume-lines.md)
- [List Languages](actions/list-sales-order-lines.md)
- [List Currencies](actions/list-sales-orders.md)
- [List Sequences](actions/list-sequences.md)
- [List Server Actions](actions/list-server-actions.md)
- [List Shift Templates](actions/list-shift-templates.md)
- [List Skill Levels](actions/list-skill-levels.md)
- [List Skill Types](actions/list-skill-types.md)
- [List Skills](actions/list-skills.md)
- [List Menus](actions/list-supplier-infos.md)
- [List Users](actions/list-users.md)
- [List Work Details](actions/list-work-details.md)
- [List Work Locations](actions/list-work-locations.md)
