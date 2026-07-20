# Odoo: Native API Reference

A consolidated summary of Odoo's API configuration and 76 documented operations, with links to official documentation.

- **Official docs:** https://www.odoo.com/documentation/19.0/developer/reference/external_api.html
- **API base URL:** `https://{domain}/json/2`

## Authentication

### API Key

Connect to an Odoo 19 JSON-2 tenant with a bearer API key plus tenant routing details.

### Credentials

- **API Key:** `apiKey` · required
- **Domain:** `domain` · required · Required Odoo tenant hostname, for example mycompany.odoo.com or your self-hosted Odoo domain.
- **Database:** `database` · optional · Optional database name. Provide this only when the tenant requires the X-Odoo-Database header.

Send these headers with each API request:

```http
X-Odoo-Database: <database>
```

[Official authentication documentation](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |
| `User-Agent` | `MindCloud Odoo integration` |

## Pagination

Use `limit` in the request body to set the page size (default 50; accepted range 1–100). Use `offset` in the request body as the record offset; numbering starts at 0.

## Filtering

Send filters in the request body.

## Sorting

Set the sort field with `order` in the request body. Only one sort field is accepted.

## Endpoints (76 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contacts](actions/create-contacts.md) | `POST /res.partner/create` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [Create Departments](actions/create-departments.md) | `POST /hr.department/create` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [Create Job Positions](actions/create-job-positions.md) | `POST /hr.job/create` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [Delete Contacts](actions/delete-contacts.md) | `POST /res.partner/unlink` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [Delete Departments](actions/delete-departments.md) | `POST /hr.department/unlink` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [Delete Job Positions](actions/delete-job-positions.md) | `POST /hr.job/unlink` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [Get Contacts By IDs](actions/get-contacts-by-ids.md) | `POST /res.partner/read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [Get Departments By IDs](actions/get-departments-by-ids.md) | `POST /hr.department/read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [Get Job Positions By IDs](actions/get-job-positions-by-ids.md) | `POST /hr.job/read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Access Controls](actions/list-access-controls.md) | `POST /ir.model.access/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Access Rules](actions/list-access-rules.md) | `POST /ir.rule/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Departments](actions/list-accounts.md) | `POST /hr.department/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Action Windows](actions/list-action-windows.md) | `POST /ir.actions.act_window/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Activities](actions/list-activities.md) | `POST /mail.activity/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Activity Types](actions/list-activity-types.md) | `POST /mail.activity.type/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Bank Accounts](actions/list-bank-accounts.md) | `POST /res.partner.bank/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Blacklisted Emails](actions/list-blacklisted-emails.md) | `POST /mail.blacklist/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Blacklisted Phone Numbers](actions/list-blacklisted-phone-numbers.md) | `POST /phone.blacklist/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List System Parameters](actions/list-campaigns.md) | `POST /ir.config_parameter/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Channel Members](actions/list-channel-members.md) | `POST /discuss.channel.member/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Companies](actions/list-companies.md) | `POST /res.company/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Contact Tags](actions/list-contact-tags.md) | `POST /res.partner.category/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Contacts](actions/list-contacts.md) | `POST /res.partner/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Contract Types](actions/list-contract-types.md) | `POST /hr.contract.type/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Countries](actions/list-countries.md) | `POST /res.country/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Country Groups](actions/list-country-groups.md) | `POST /res.country.group/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Country States](actions/list-country-states.md) | `POST /res.country.state/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Currency Rates](actions/list-currency-rates.md) | `POST /res.currency.rate/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Departure Reasons](actions/list-departure-reasons.md) | `POST /hr.departure.reason/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Discussion Categories](actions/list-discussion-categories.md) | `POST /discuss.category/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Discussion Channels](actions/list-discussion-channels.md) | `POST /discuss.channel/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Email Aliases](actions/list-email-aliases.md) | `POST /mail.alias/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Email Domains](actions/list-email-domains.md) | `POST /mail.alias.domain/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Email Templates](actions/list-email-templates.md) | `POST /mail.template/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Employee Categories](actions/list-employee-categories.md) | `POST /hr.employee.category/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Employee Locations](actions/list-employee-locations.md) | `POST /hr.employee.location/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Employee Skills](actions/list-employee-skills.md) | `POST /hr.employee.skill/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Employees](actions/list-employees.md) | `POST /hr.employee/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Field Selections](actions/list-field-selections.md) | `POST /ir.model.fields.selection/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Job Positions](actions/list-job-positions.md) | `POST /hr.job/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Attachments](actions/list-journal-entries.md) | `POST /ir.attachment/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Messages](actions/list-journal-entry-lines.md) | `POST /mail.message/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Scheduled Actions](actions/list-leads.md) | `POST /ir.cron/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Logs](actions/list-logs.md) | `POST /ir.logging/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Mail Servers](actions/list-mail-servers.md) | `POST /ir.mail_server/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Message Notifications](actions/list-message-notifications.md) | `POST /mail.notification/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Message Subtypes](actions/list-message-subtypes.md) | `POST /mail.message.subtype/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Model Constraints](actions/list-model-constraints.md) | `POST /ir.model.constraint/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Module Categories](actions/list-module-categories.md) | `POST /ir.module.category/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Models](actions/list-payment-terms.md) | `POST /ir.model/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Planning Roles](actions/list-planning-roles.md) | `POST /planning.role/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Planning Shifts](actions/list-planning-shifts.md) | `POST /planning.slot/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Views](actions/list-pricelists.md) | `POST /ir.ui.view/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Model Data](actions/list-product-categories.md) | `POST /ir.model.data/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Modules](actions/list-product-templates.md) | `POST /ir.module.module/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Model Fields](actions/list-products.md) | `POST /ir.model.fields/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Industries](actions/list-purchase-order-lines.md) | `POST /res.partner.industry/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Groups](actions/list-purchase-orders.md) | `POST /res.groups/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Resource Calendars](actions/list-resource-calendars.md) | `POST /resource.calendar/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Resume Line Types](actions/list-resume-line-types.md) | `POST /hr.resume.line.type/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Resume Lines](actions/list-resume-lines.md) | `POST /hr.resume.line/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Languages](actions/list-sales-order-lines.md) | `POST /res.lang/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Currencies](actions/list-sales-orders.md) | `POST /res.currency/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Sequences](actions/list-sequences.md) | `POST /ir.sequence/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Server Actions](actions/list-server-actions.md) | `POST /ir.actions.server/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Shift Templates](actions/list-shift-templates.md) | `POST /planning.slot.template/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Skill Levels](actions/list-skill-levels.md) | `POST /hr.skill.level/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Skill Types](actions/list-skill-types.md) | `POST /hr.skill.type/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Skills](actions/list-skills.md) | `POST /hr.skill/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Menus](actions/list-supplier-infos.md) | `POST /ir.ui.menu/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Users](actions/list-users.md) | `POST /res.users/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Work Details](actions/list-work-details.md) | `POST /resource.calendar.attendance/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [List Work Locations](actions/list-work-locations.md) | `POST /hr.work.location/search_read` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [Update Contacts](actions/update-contacts.md) | `POST /res.partner/write` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [Update Departments](actions/update-departments.md) | `POST /hr.department/write` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
| [Update Job Positions](actions/update-job-positions.md) | `POST /hr.job/write` | [docs](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html) |
