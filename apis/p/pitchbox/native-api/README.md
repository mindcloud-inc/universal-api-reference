# Pitchbox: Native API Reference

A consolidated summary of Pitchbox's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://apiv2.pitchbox.com/docs
- **OpenAPI specification:** https://apiv2.pitchbox.com/swagger.json?v=20
- **API base URL:** `https://apiv2.pitchbox.com`

## Authentication

### API Key

Use a Pitchbox API key (JWT) created in the Pitchbox UI.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.pitchbox.com/article/42-how-do-i-retrieve-my-pitchbox-api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The current page number is read from `page`.

## Pagination

Use `limit` in the query string to set the page size (default 100; maximum 1000). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Campaign Tag](actions/add-campaign-tag.md) | `POST /api/campaigns/:campaignId/tags` | [docs](https://apiv2.pitchbox.com/docs) |
| [Create Metrics Filter Template](actions/create-metrics-filter-template.md) | `POST /api/metric_filter_templates` | [docs](https://apiv2.pitchbox.com/docs) |
| [Delete Campaign Tag](actions/delete-campaign-tag.md) | `DELETE /api/campaigns/:campaignId/tags/:tagId` | [docs](https://apiv2.pitchbox.com/docs) |
| [Delete Metrics Filter Template](actions/delete-metrics-filter-template.md) | `DELETE /api/metric_filter_templates/:id` | [docs](https://apiv2.pitchbox.com/docs) |
| [Get Campaign By Id](actions/get-campaign-by-id.md) | `GET /api/campaigns/:id` | [docs](https://apiv2.pitchbox.com/docs) |
| [Get Campaign Outreach Settings](actions/get-campaign-outreach-settings.md) | `GET /api/campaigns/:campaignId/outreach_settings` | [docs](https://apiv2.pitchbox.com/docs) |
| [Get Contact By Id](actions/get-contact-by-id.md) | `GET /api/contacts/:id` | [docs](https://apiv2.pitchbox.com/docs) |
| [Get My Profile](actions/get-my-profile.md) | `GET /api/me` | [docs](https://apiv2.pitchbox.com/docs) |
| [Get Opportunity By Id](actions/get-opportunity-by-id.md) | `GET /api/opportunities/:id` | [docs](https://apiv2.pitchbox.com/docs) |
| [Get Reports Info](actions/get-reports-info.md) | `GET /api/reports` | [docs](https://apiv2.pitchbox.com/docs) |
| [List Campaigns](actions/list-campaigns.md) | `GET /api/campaigns` | [docs](https://apiv2.pitchbox.com/docs) |
| [List Contacts](actions/list-contacts.md) | `GET /api/contacts` | [docs](https://apiv2.pitchbox.com/docs) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /api/custom_fields` | [docs](https://apiv2.pitchbox.com/docs) |
| [List Discovery Types](actions/list-discovery-types.md) | `GET /api/discovery_types` | [docs](https://apiv2.pitchbox.com/docs) |
| [List Email Accounts](actions/list-email-accounts.md) | `GET /api/email_accounts` | [docs](https://apiv2.pitchbox.com/docs) |
| [List Form Submissions](actions/list-form-submissions.md) | `GET /api/form_submissions` | [docs](https://apiv2.pitchbox.com/docs) |
| [List Inbound Emails](actions/list-inbound-emails.md) | `GET /api/inbound_emails` | [docs](https://apiv2.pitchbox.com/docs) |
| [List Metrics Filter Templates](actions/list-metrics-filter-templates.md) | `GET /api/metric_filter_templates` | [docs](https://apiv2.pitchbox.com/docs) |
| [List Opportunities](actions/list-opportunities.md) | `GET /api/opportunities` | [docs](https://apiv2.pitchbox.com/docs) |
| [List Opportunity Custom Field Values](actions/list-opportunity-custom-field-values.md) | `GET /api/opportunities/:opportunityId/custom_fields` | [docs](https://apiv2.pitchbox.com/docs) |
| [List Opportunity Milestone History](actions/list-opportunity-milestone-history.md) | `GET /api/opportunities/:opportunityId/milestone_history` | [docs](https://apiv2.pitchbox.com/docs) |
| [List Opportunity Milestones](actions/list-opportunity-milestones.md) | `GET /api/milestones` | [docs](https://apiv2.pitchbox.com/docs) |
| [List Opportunity Personalization Field Values](actions/list-opportunity-personalization-field-values.md) | `GET /api/opportunities/:opportunityId/personalization` | [docs](https://apiv2.pitchbox.com/docs) |
| [List Outreach Emails](actions/list-outreach-emails.md) | `GET /api/outreach_emails` | [docs](https://apiv2.pitchbox.com/docs) |
| [List Personalization Fields](actions/list-personalization-fields.md) | `GET /api/personalization` | [docs](https://apiv2.pitchbox.com/docs) |
| [List Projects](actions/list-projects.md) | `GET /api/projects` | [docs](https://apiv2.pitchbox.com/docs) |
| [List Sent Reply Emails](actions/list-sent-reply-emails.md) | `GET /api/sent_replies` | [docs](https://apiv2.pitchbox.com/docs) |
| [List Tags](actions/list-tags.md) | `GET /api/tags` | [docs](https://apiv2.pitchbox.com/docs) |
| [List Tasks](actions/list-tasks.md) | `GET /api/tasks` | [docs](https://apiv2.pitchbox.com/docs) |
| [Update Metrics Filter Template](actions/update-metrics-filter-template.md) | `PUT /api/metric_filter_templates/:id` | [docs](https://apiv2.pitchbox.com/docs) |
