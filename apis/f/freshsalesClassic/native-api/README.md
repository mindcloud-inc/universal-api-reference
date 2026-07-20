# Freshsales Classic: Native API Reference

A consolidated summary of Freshsales Classic's API configuration and 29 documented operations, with links to official documentation.

- **Official docs:** https://developers.freshworks.com/crm/api/
- **API base URL:** `https://{bundleAlias}/api`

## Authentication

### API Key

Use your Freshsales Classic CRM API key together with your Freshworks CRM bundle alias.

### Credentials

- **API Key:** `apiKey` · required
- **Bundle Alias:** `bundleAlias` · required · Your Freshworks CRM bundle alias, for example yourcompany.myfreshworks.com/crm/sales.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.freshworks.com/crm/api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (29 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Account Views](actions/list-account-views.md) | `GET /sales_accounts/filters` | [docs](https://developers.freshworks.com/crm/api/#list_all_accounts) |
| [List All Account Fields](actions/list-all-account-fields.md) | `GET /settings/sales_accounts/fields` | [docs](https://developers.freshworks.com/crm/api/#list_all_account_fields) |
| [List All Accounts](actions/list-all-accounts.md) | `GET /sales_accounts/view/:viewId` | [docs](https://developers.freshworks.com/crm/api/#list_all_accounts) |
| [List All Appointments](actions/list-all-appointments.md) | `GET /appointments` | [docs](https://developers.freshworks.com/crm/api/#list_all_appointment) |
| [List All Contact Fields](actions/list-all-contact-fields.md) | `GET /settings/contacts/fields` | [docs](https://developers.freshworks.com/crm/api/#list_all_contact_fields) |
| [List All Contacts](actions/list-all-contacts.md) | `GET /contacts/view/:viewId` | [docs](https://developers.freshworks.com/crm/api/#list_all_contacts) |
| [List All Deal Fields](actions/list-all-deal-fields.md) | `GET /settings/deals/fields` | [docs](https://developers.freshworks.com/crm/api/#list_all_deal_fields) |
| [List All Deals](actions/list-all-deals.md) | `GET /deals/view/:viewId` | [docs](https://developers.freshworks.com/crm/api/#list_all_deals) |
| [List All Sales Activities](actions/list-all-sales-activities.md) | `GET /sales_activities` | [docs](https://developers.freshworks.com/crm/api/#list_all_sales_activities) |
| [List All Sales Activity Fields](actions/list-all-sales-activity-fields.md) | `GET /settings/sales_activities/fields` | [docs](https://developers.freshworks.com/crm/api/#list_all_sales_activity_fields) |
| [List All Tasks](actions/list-all-tasks.md) | `GET /tasks` | [docs](https://developers.freshworks.com/crm/api/#list_all_task) |
| [List Campaigns](actions/list-campaigns.md) | `GET /selector/campaigns` | [docs](https://developers.freshworks.com/crm/api/#admin_configuration) |
| [List Contact Activities](actions/list-contact-activities.md) | `GET /contacts/:id/activities` | [docs](https://developers.freshworks.com/crm/api/#list_all_contact_activities) |
| [List Contact Statuses](actions/list-contact-statuses.md) | `GET /selector/contact_statuses` | [docs](https://developers.freshworks.com/crm/api/#admin_configuration) |
| [List Contact Views](actions/list-contact-views.md) | `GET /contacts/filters` | [docs](https://developers.freshworks.com/crm/api/#list_all_contacts) |
| [List Deal Pipelines](actions/list-deal-pipelines.md) | `GET /selector/deal_pipelines` | [docs](https://developers.freshworks.com/crm/api/#admin_configuration) |
| [List Deal Stages](actions/list-deal-stages.md) | `GET /selector/deal_stages` | [docs](https://developers.freshworks.com/crm/api/#admin_configuration) |
| [List Deal Views](actions/list-deal-views.md) | `GET /deals/filters` | [docs](https://developers.freshworks.com/crm/api/#list_all_deals) |
| [List Lifecycle Stages](actions/list-lifecycle-stages.md) | `GET /selector/lifecycle_stages` | [docs](https://developers.freshworks.com/crm/api/#admin_configuration) |
| [List Owners](actions/list-owners.md) | `GET /selector/owners` | [docs](https://developers.freshworks.com/crm/api/#admin_configuration) |
| [List Sales Activity Types](actions/list-sales-activity-types.md) | `GET /selector/sales_activity_types` | [docs](https://developers.freshworks.com/crm/api/#admin_configuration) |
| [Lookup Search](actions/lookup-search.md) | `GET /lookup` | [docs](https://developers.freshworks.com/crm/api/#lookup_search) |
| [Search](actions/search.md) | `GET /search` | [docs](https://developers.freshworks.com/crm/api/#search) |
| [View a Contact](actions/view-a-contact.md) | `GET /contacts/:id` | [docs](https://developers.freshworks.com/crm/api/#view_a_contact) |
| [View a Deal](actions/view-a-deal.md) | `GET /deals/:id` | [docs](https://developers.freshworks.com/crm/api/#view_a_deal) |
| [View a Sales Activity](actions/view-a-sales-activity.md) | `GET /sales_activities/:salesActivityId` | [docs](https://developers.freshworks.com/crm/api/#view_a_sales_activity) |
| [View a Task](actions/view-a-task.md) | `GET /tasks/:id` | [docs](https://developers.freshworks.com/crm/api/#view_task) |
| [View an Account](actions/view-an-account.md) | `GET /sales_accounts/:id` | [docs](https://developers.freshworks.com/crm/api/#view_account) |
| [View an Appointment](actions/view-an-appointment.md) | `GET /appointments/:appointmentId` | [docs](https://developers.freshworks.com/crm/api/#view_an_appointment) |
