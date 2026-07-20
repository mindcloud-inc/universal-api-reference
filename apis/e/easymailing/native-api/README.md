# Easymailing: Native API Reference

A consolidated summary of Easymailing's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://developers.easymailing.com/
- **OpenAPI specification:** https://developers.easymailing.com/docs?format=json
- **API base URL:** `https://api.easymailing.com`

## Authentication

### API Key

Use an Easymailing API key sent in the X-Auth-Token header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Auth-Token: <apiKey>
```

[Official authentication documentation](https://developers.easymailing.com/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/ld+json` |
| `Content-Type` | `application/ld+json` |

Responses from this API use JSON.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Audience](actions/get-audience.md) | `GET /audiences/{{uuid}}` | [docs](https://developers.easymailing.com/) |
| [Get Audience Member](actions/get-audience-member.md) | `GET /audiences/{{audienceUuid}}/members/{{uuid}}` | [docs](https://developers.easymailing.com/) |
| [Get Automation](actions/get-automation.md) | `GET /automations/{{uuid}}` | [docs](https://developers.easymailing.com/) |
| [Get Automation Queue](actions/get-automation-queue.md) | `GET /automations/{{automationUuid}}/automation_queues/{{uuid}}` | [docs](https://developers.easymailing.com/) |
| [Get Campaign](actions/get-campaign.md) | `GET /campaigns/{{uuid}}` | [docs](https://developers.easymailing.com/) |
| [Get Condition Field](actions/get-condition-field.md) | `GET /audiences/{{audienceUuid}}/condition_fields/{{uuid}}` | [docs](https://developers.easymailing.com/) |
| [Get Custom Field](actions/get-custom-field.md) | `GET /audiences/{{audienceUuid}}/list_fields/{{uuid}}` | [docs](https://developers.easymailing.com/) |
| [Get Group](actions/get-group.md) | `GET /audiences/{{audienceUuid}}/groups/{{uuid}}` | [docs](https://developers.easymailing.com/) |
| [Get Invoice](actions/get-invoice.md) | `GET /invoices/{{uuid}}` | [docs](https://developers.easymailing.com/) |
| [Get My Subscription](actions/get-my-subscription.md) | `GET /my_suscription` | [docs](https://developers.easymailing.com/) |
| [Get Segment](actions/get-segment.md) | `GET /audiences/{{audienceUuid}}/list_segments/{{uuid}}` | [docs](https://developers.easymailing.com/) |
| [Get Subscription Form](actions/get-subscription-form.md) | `GET /audiences/{{audienceUuid}}/suscription_forms/{{uuid}}` | [docs](https://developers.easymailing.com/) |
| [Get Subscription Form Publishing Info](actions/get-subscription-form-publishing-info.md) | `GET /audiences/{{audienceUuid}}/suscription_forms/{{uuid}}/publishing-info` | [docs](https://developers.easymailing.com/) |
| [Get Template](actions/get-template.md) | `GET /templates/{{uuid}}` | [docs](https://developers.easymailing.com/) |
| [Get Template Schema](actions/get-template-schema.md) | `GET /templates-schema` | [docs](https://developers.easymailing.com/) |
| [List Audience Members](actions/list-audience-members.md) | `GET /audiences/{{audienceUuid}}/members` | [docs](https://developers.easymailing.com/) |
| [List Audiences](actions/list-audiences.md) | `GET /audiences` | [docs](https://developers.easymailing.com/) |
| [List Automation Queues](actions/list-automation-queues.md) | `GET /automations/{{automationUuid}}/automation_queues` | [docs](https://developers.easymailing.com/) |
| [List Automations](actions/list-automations.md) | `GET /automations` | [docs](https://developers.easymailing.com/) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://developers.easymailing.com/) |
| [List Condition Fields](actions/list-condition-fields.md) | `GET /audiences/{{audienceUuid}}/condition_fields` | [docs](https://developers.easymailing.com/) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /audiences/{{audienceUuid}}/list_fields` | [docs](https://developers.easymailing.com/) |
| [List Groups](actions/list-groups.md) | `GET /audiences/{{audienceUuid}}/groups` | [docs](https://developers.easymailing.com/) |
| [List Invoices](actions/list-invoices.md) | `GET /invoices` | [docs](https://developers.easymailing.com/) |
| [List Member Activities](actions/list-member-activities.md) | `GET /audiences/{{audienceUuid}}/members/{{memberUuid}}/activities` | [docs](https://developers.easymailing.com/) |
| [List Segments](actions/list-segments.md) | `GET /audiences/{{audienceUuid}}/list_segments` | [docs](https://developers.easymailing.com/) |
| [List Subscription Forms](actions/list-subscription-forms.md) | `GET /audiences/{{audienceUuid}}/suscription_forms` | [docs](https://developers.easymailing.com/) |
| [List Support Tickets](actions/list-support-tickets.md) | `GET /support/tickets` | [docs](https://developers.easymailing.com/) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://developers.easymailing.com/) |
| [Search Members](actions/search-members.md) | `GET /members/search` | [docs](https://developers.easymailing.com/) |
