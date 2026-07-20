# RD Station Marketing: Native API Reference

A consolidated summary of RD Station Marketing's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developers.rdstation.com/reference/introducao-rdsm
- **API base URL:** `https://api.rd.services`

## Authentication

### OAuth2

OAuth2 authorization code flow for RD Station Marketing API

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://api.rd.services/auth/dialog to approve access.
2. Exchange the returned authorization code with a POST request to https://api.rd.services/auth/token?token_by=code.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.rd.services/auth/token.

[Official authentication documentation](https://developers.rdstation.com/reference/gerar-code)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `fields`.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Leads to Workflow](actions/add-leads-to-workflow.md) | `POST /platform/workflows/:id/leads` | [docs](https://developers.rdstation.com/reference/post_platform-workflows-id-leads) |
| [Add Tag to Contact by UUID or Email](actions/add-tag-to-contact-by-uuid-or-email.md) | `POST /platform/contacts/:identifier::value/tag` | [docs](https://developers.rdstation.com/reference/post_platform-contacts-identifier-value-tag) |
| [Create Contact](actions/create-contact.md) | `POST /platform/contacts` | [docs](https://developers.rdstation.com/reference/post_platform-contacts) |
| [Create Custom Field](actions/create-custom-field.md) | `POST /platform/contacts/fields` | [docs](https://developers.rdstation.com/reference/post_platform-contacts-fields) |
| [Delete Contact by UUID or Email](actions/delete-contact-by-uuid-or-email.md) | `DELETE /platform/contacts/:identifier::value` | [docs](https://developers.rdstation.com/reference/delete_platform-contacts-identifier-value) |
| [Delete Custom Field](actions/delete-custom-field.md) | `DELETE /platform/contacts/fields/:uuid` | [docs](https://developers.rdstation.com/reference/delete_platform-contacts-fields-uuid) |
| [Get Contact by UUID or Email](actions/get-contact-by-uuid-or-email.md) | `GET /platform/contacts/:identifier::value` | [docs](https://developers.rdstation.com/reference/get_platform-contacts-identifier-value) |
| [Get Contact Default Funnel by UUID or Email](actions/get-contact-default-funnel-by-uuid-or-email.md) | `GET /platform/contacts/:identifier::value/funnels/default` | [docs](https://developers.rdstation.com/reference/get_platform-contacts-identifier-value-funnels-default) |
| [Get Conversion Asset Statistics](actions/get-conversion-asset-statistics.md) | `GET /platform/analytics/conversions` | [docs](https://developers.rdstation.com/reference/get_platform-analytics-conversions) |
| [Get Email by ID](actions/get-email-by-id.md) | `GET /platform/emails/:id` | [docs](https://developers.rdstation.com/reference/get_platform-emails-id) |
| [Get Email Marketing Statistics](actions/get-email-marketing-statistics.md) | `GET /platform/analytics/emails` | [docs](https://developers.rdstation.com/reference/get_platform-analytics-emails) |
| [Get Workflow by ID](actions/get-workflow-by-id.md) | `GET /platform/workflows/:id` | [docs](https://developers.rdstation.com/reference/get_platform-workflows-id) |
| [List Contact Events](actions/list-contact-events.md) | `GET /platform/contacts/:uuid/events` | [docs](https://developers.rdstation.com/reference/get_platform-contacts-uuid-events) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /platform/contacts/fields` | [docs](https://developers.rdstation.com/reference/get_platform-contacts-fields) |
| [List Emails](actions/list-emails.md) | `GET /platform/emails` | [docs](https://developers.rdstation.com/reference/get_platform-emails) |
| [List Forms](actions/list-forms.md) | `GET /platform/embeddables` | [docs](https://developers.rdstation.com/reference/get_platform-embeddables) |
| [List Landing Pages](actions/list-landing-pages.md) | `GET /platform/landing_pages` | [docs](https://developers.rdstation.com/reference/get_platform-landing-pages) |
| [List Popups](actions/list-popups.md) | `GET /platform/popups` | [docs](https://developers.rdstation.com/reference/get_platform-popups) |
| [List Segmentation Contacts](actions/list-segmentation-contacts.md) | `GET /platform/segmentations/:id/contacts` | [docs](https://developers.rdstation.com/reference/get_platform-segmentations-id-contacts) |
| [List Segmentations](actions/list-segmentations.md) | `GET /platform/segmentations` | [docs](https://developers.rdstation.com/reference/get_platform-segmentations) |
| [List Workflows](actions/list-workflows.md) | `GET /platform/workflows` | [docs](https://developers.rdstation.com/reference/get_platform-workflows) |
| [Update Contact by UUID or Email](actions/update-contact-by-uuid-or-email.md) | `PATCH /platform/contacts/:identifier::value` | [docs](https://developers.rdstation.com/reference/patch_platform-contacts-identifier-value) |
| [Update Contact Default Funnel by UUID or Email](actions/update-contact-default-funnel-by-uuid-or-email.md) | `PUT /platform/contacts/:identifier::value/funnels/default` | [docs](https://developers.rdstation.com/reference/put_platform-contacts-identifier-value-funnels-default) |
| [Update Custom Field](actions/update-custom-field.md) | `PATCH /platform/contacts/fields/:uuid` | [docs](https://developers.rdstation.com/reference/patch_platform-contacts-fields-uuid) |
