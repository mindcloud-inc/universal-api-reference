# <img src="https://images.mindcloud.co/apps/icons/odoo-new_1775832846998.png" alt="Odoo logo" width="28" height="28"> Odoo: Universal API

Odoo JSON-2 API integration for reading and mutating ERP records across core business models.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/odoo/latest
- **Category:** Commerce / ERP
- **Actions:** 76
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.odoo.com
- **Vendor API docs:** https://www.odoo.com/documentation/19.0/developer/reference/external_api.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/odoo/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (76)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [List Companies](actions/list-companies.md) | GET | Retrieves companies from Odoo. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contacts](actions/create-contacts.md) | POST | Creates new contacts in Odoo. |
| [Create Departments](actions/create-departments.md) | POST | Creates new departments in Odoo. |
| [Create Job Positions](actions/create-job-positions.md) | POST | Creates new job positions in Odoo. |
| [Delete Contacts](actions/delete-contacts.md) | DELETE | Deletes contacts from Odoo. |
| [Delete Departments](actions/delete-departments.md) | DELETE | Deletes departments from Odoo. |
| [Delete Job Positions](actions/delete-job-positions.md) | DELETE | Deletes job positions from Odoo. |
| [Get Contacts By IDs](actions/get-contacts-by-ids.md) | GET | Retrieves contacts by ID from Odoo. |
| [Get Departments By IDs](actions/get-departments-by-ids.md) | GET | Retrieves departments by ID from Odoo. |
| [Get Job Positions By IDs](actions/get-job-positions-by-ids.md) | GET | Retrieves job positions by ID from Odoo. |
| [List Access Controls](actions/list-access-controls.md) | GET | Retrieves access controls from Odoo. |
| [List Access Rules](actions/list-access-rules.md) | GET | Retrieves access rules from Odoo. |
| [List Departments](actions/list-accounts.md) | GET | Retrieves departments from Odoo. |
| [List Action Windows](actions/list-action-windows.md) | GET | Retrieves action windows from Odoo. |
| [List Activities](actions/list-activities.md) | GET | Retrieves activities from Odoo. |
| [List Activity Types](actions/list-activity-types.md) | GET | Retrieves activity types from Odoo. |
| [List Bank Accounts](actions/list-bank-accounts.md) | GET | Retrieves bank accounts from Odoo. |
| [List Blacklisted Emails](actions/list-blacklisted-emails.md) | GET | Retrieves blacklisted emails from Odoo. |
| [List Blacklisted Phone Numbers](actions/list-blacklisted-phone-numbers.md) | GET | Retrieves blacklisted phone numbers from Odoo. |
| [List System Parameters](actions/list-campaigns.md) | GET | Retrieves system parameters from Odoo. |
| [List Channel Members](actions/list-channel-members.md) | GET | Retrieves channel members from Odoo. |
| [List Contact Tags](actions/list-contact-tags.md) | GET | Retrieves contact tags from Odoo. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Odoo. |
| [List Contract Types](actions/list-contract-types.md) | GET | Retrieves contract types from Odoo. |
| [List Countries](actions/list-countries.md) | GET | Retrieves countries from Odoo. |
| [List Country Groups](actions/list-country-groups.md) | GET | Retrieves country groups from Odoo. |
| [List Country States](actions/list-country-states.md) | GET | Retrieves country states from Odoo. |
| [List Currency Rates](actions/list-currency-rates.md) | GET | Retrieves currency rates from Odoo. |
| [List Departure Reasons](actions/list-departure-reasons.md) | GET | Retrieves departure reasons from Odoo. |
| [List Discussion Categories](actions/list-discussion-categories.md) | GET | Retrieves discussion categories from Odoo. |
| [List Discussion Channels](actions/list-discussion-channels.md) | GET | Retrieves discussion channels from Odoo. |
| [List Email Aliases](actions/list-email-aliases.md) | GET | Retrieves email aliases from Odoo. |
| [List Email Domains](actions/list-email-domains.md) | GET | Retrieves email domains from Odoo. |
| [List Email Templates](actions/list-email-templates.md) | GET | Retrieves email templates from Odoo. |
| [List Employee Categories](actions/list-employee-categories.md) | GET | Retrieves employee categories from Odoo. |
| [List Employee Locations](actions/list-employee-locations.md) | GET | Retrieves employee locations from Odoo. |
| [List Employee Skills](actions/list-employee-skills.md) | GET | Retrieves employee skills from Odoo. |
| [List Employees](actions/list-employees.md) | GET | Retrieves employees from Odoo. |
| [List Field Selections](actions/list-field-selections.md) | GET | Retrieves field selections from Odoo. |
| [List Job Positions](actions/list-job-positions.md) | GET | Retrieves job positions from Odoo. |
| [List Attachments](actions/list-journal-entries.md) | GET | Retrieves attachments from Odoo. |
| [List Messages](actions/list-journal-entry-lines.md) | GET | Retrieves messages from Odoo. |
| [List Scheduled Actions](actions/list-leads.md) | GET | Retrieves scheduled actions from Odoo. |
| [List Logs](actions/list-logs.md) | GET | Retrieves logs from Odoo. |
| [List Mail Servers](actions/list-mail-servers.md) | GET | Retrieves mail servers from Odoo. |
| [List Message Notifications](actions/list-message-notifications.md) | GET | Retrieves message notifications from Odoo. |
| [List Message Subtypes](actions/list-message-subtypes.md) | GET | Retrieves message subtypes from Odoo. |
| [List Model Constraints](actions/list-model-constraints.md) | GET | Retrieves model constraints from Odoo. |
| [List Module Categories](actions/list-module-categories.md) | GET | Retrieves module categories from Odoo. |
| [List Models](actions/list-payment-terms.md) | GET | Retrieves models from Odoo. |
| [List Planning Roles](actions/list-planning-roles.md) | GET | Retrieves planning roles from Odoo. |
| [List Planning Shifts](actions/list-planning-shifts.md) | GET | Retrieves planning shifts from Odoo. |
| [List Views](actions/list-pricelists.md) | GET | Retrieves views from Odoo. |
| [List Model Data](actions/list-product-categories.md) | GET | Retrieves model data from Odoo. |
| [List Modules](actions/list-product-templates.md) | GET | Retrieves modules from Odoo. |
| [List Model Fields](actions/list-products.md) | GET | Retrieves model fields from Odoo. |
| [List Industries](actions/list-purchase-order-lines.md) | GET | Retrieves industries from Odoo. |
| [List Groups](actions/list-purchase-orders.md) | GET | Retrieves groups from Odoo. |
| [List Resource Calendars](actions/list-resource-calendars.md) | GET | Retrieves resource calendars from Odoo. |
| [List Resume Line Types](actions/list-resume-line-types.md) | GET | Retrieves resume line types from Odoo. |
| [List Resume Lines](actions/list-resume-lines.md) | GET | Retrieves resume lines from Odoo. |
| [List Languages](actions/list-sales-order-lines.md) | GET | Retrieves languages from Odoo. |
| [List Currencies](actions/list-sales-orders.md) | GET | Retrieves currencies from Odoo. |
| [List Sequences](actions/list-sequences.md) | GET | Retrieves sequences from Odoo. |
| [List Server Actions](actions/list-server-actions.md) | GET | Retrieves server actions from Odoo. |
| [List Shift Templates](actions/list-shift-templates.md) | GET | Retrieves shift templates from Odoo. |
| [List Skill Levels](actions/list-skill-levels.md) | GET | Retrieves skill levels from Odoo. |
| [List Skill Types](actions/list-skill-types.md) | GET | Retrieves skill types from Odoo. |
| [List Skills](actions/list-skills.md) | GET | Retrieves skills from Odoo. |
| [List Menus](actions/list-supplier-infos.md) | GET | Retrieves menus from Odoo. |
| [List Work Details](actions/list-work-details.md) | GET | Retrieves work details from Odoo. |
| [List Work Locations](actions/list-work-locations.md) | GET | Retrieves work locations from Odoo. |
| [Update Contacts](actions/update-contacts.md) | PUT | Updates existing contacts in Odoo. |
| [Update Departments](actions/update-departments.md) | PUT | Updates existing departments in Odoo. |
| [Update Job Positions](actions/update-job-positions.md) | PUT | Updates existing job positions in Odoo. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from Odoo. |

