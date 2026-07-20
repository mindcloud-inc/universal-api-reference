# Constant Contact: Native API Reference

A consolidated summary of Constant Contact's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://developer.constantcontact.com/api_guide/index.html
- **OpenAPI specification:** https://api.cc.email/v3/swagger.yaml
- **API base URL:** `https://api.cc.email/v3`

## Authentication

### OAuth2

OAuth2 authorization code flow for Constant Contact API access.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://authz.constantcontact.com/oauth2/default/v1/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://authz.constantcontact.com/oauth2/default/v1/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `account_read account_update contact_data campaign_data offline_access`.

PKCE is enabled. The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://authz.constantcontact.com/oauth2/default/v1/token.

[Official authentication documentation](https://developer.constantcontact.com/api_guide/auth_overview.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `contacts`.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–500).

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://developer.constantcontact.com/api_guide/contacts_post_one.html) |
| [Create Contact Custom Field](actions/create-contact-custom-field.md) | `POST /contact_custom_fields` | [docs](https://developer.constantcontact.com/api_guide/create_custom_fields.html) |
| [Create Contact List](actions/create-contact-list.md) | `POST /contact_lists` | [docs](https://developer.constantcontact.com/api_guide/lists_post.html) |
| [Create Contact Tag](actions/create-contact-tag.md) | `POST /contact_tags` | [docs](https://developer.constantcontact.com/api_guide/tags_create.html) |
| [Create Email Campaign](actions/create-email-campaign.md) | `POST /emails` | [docs](https://developer.constantcontact.com/api_guide/email_campaign_create.html) |
| [Create or Update Contact](actions/create-or-update-contact.md) | `POST /contacts/sign_up_form` | [docs](https://developer.constantcontact.com/api_guide/contacts_create_or_update.html) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/:contact_id` | [docs](https://developer.constantcontact.com/api_guide/contacts_delete.html) |
| [Delete Contact Custom Field](actions/delete-contact-custom-field.md) | `DELETE /contact_custom_fields/:custom_field_id` | [docs](https://developer.constantcontact.com/api_guide/delete_custom_fields.html) |
| [Delete Contact List](actions/delete-contact-list.md) | `DELETE /contact_lists/:list_id` | [docs](https://developer.constantcontact.com/api_guide/lists_delete.html) |
| [Delete Contact Tag](actions/delete-contact-tag.md) | `DELETE /contact_tags/:tag_id` | [docs](https://developer.constantcontact.com/api_guide/tags_delete.html) |
| [Delete Email Campaign](actions/delete-email-campaign.md) | `DELETE /emails/:campaign_id` | [docs](https://developer.constantcontact.com/api_guide/email_campaigns_delete.html) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:contact_id` | [docs](https://developer.constantcontact.com/api_guide/contacts_get_one.html) |
| [Get Contact Consent Counts](actions/get-contact-consent-counts.md) | `GET /contacts/counts` | [docs](https://developer.constantcontact.com/api_guide/contacts_counts.html) |
| [Get Contact List](actions/get-contact-list.md) | `GET /contact_lists/:list_id` | [docs](https://developer.constantcontact.com/api_guide/lists_get_single.html) |
| [Get Contact Tag](actions/get-contact-tag.md) | `GET /contact_tags/:tag_id` | [docs](https://developer.constantcontact.com/api_guide/tags_get_single.html) |
| [Get Email Campaign](actions/get-email-campaign.md) | `GET /emails/:campaign_id` | [docs](https://developer.constantcontact.com/api_guide/email_campaign_id.html) |
| [Get Email Campaign Activity](actions/get-email-campaign-activity.md) | `GET /emails/activities/:campaign_activity_id` | [docs](https://developer.constantcontact.com/api_guide/email_campaigns_activity_id.html) |
| [Get Email Campaign Summary Report](actions/get-email-campaign-summary-report.md) | `GET /reports/summary_reports/email_campaign_summaries` | [docs](https://developer.constantcontact.com/api_guide/email_bulk_campaign_summary_report.html) |
| [List Contact Custom Fields](actions/list-contact-custom-fields.md) | `GET /contact_custom_fields` | [docs](https://developer.constantcontact.com/api_guide/get_custom_fields.html) |
| [List Contact Lists](actions/list-contact-lists.md) | `GET /contact_lists` | [docs](https://developer.constantcontact.com/api_guide/lists_get_all.html) |
| [List Contact Tags](actions/list-contact-tags.md) | `GET /contact_tags` | [docs](https://developer.constantcontact.com/api_guide/tags_get.html) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://developer.constantcontact.com/api_guide/contacts_get_collection.html) |
| [List Email Campaigns](actions/list-email-campaigns.md) | `GET /emails` | [docs](https://developer.constantcontact.com/api_guide/email_campaigns_collection.html) |
| [Rename Email Campaign](actions/rename-email-campaign.md) | `PATCH /emails/:campaign_id` | [docs](https://developer.constantcontact.com/api_guide/email_campaigns_rename.html) |
| [Resubscribe Contact](actions/resubscribe-contact.md) | `PUT /contacts/resubscribe/:contact_id` | [docs](https://developer.constantcontact.com/api_guide/contacts_re-subscribe.html) |
| [Schedule Email Campaign Activity](actions/schedule-email-campaign-activity.md) | `POST /emails/activities/:campaign_activity_id/schedules` | [docs](https://developer.constantcontact.com/api_guide/email_campaign_create_schedule.html) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/:contact_id` | [docs](https://developer.constantcontact.com/api_guide/contacts_put.html) |
| [Update Contact Custom Field](actions/update-contact-custom-field.md) | `PUT /contact_custom_fields/:custom_field_id` | [docs](https://developer.constantcontact.com/api_guide/create_custom_fields.html) |
| [Update Contact List](actions/update-contact-list.md) | `PUT /contact_lists/:list_id` | [docs](https://developer.constantcontact.com/api_guide/lists_put.html) |
| [Update Contact Tag](actions/update-contact-tag.md) | `PUT /contact_tags/:tag_id` | [docs](https://developer.constantcontact.com/api_guide/tags_update.html) |
