# Calendly: Native API Reference

A consolidated summary of Calendly's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://developer.calendly.com/api-docs
- **API base URL:** `https://api.calendly.com`

## Authentication

### OAuth 2.0

Calendly OAuth2 for multi-tenant/public connections

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://auth.calendly.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://auth.calendly.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `default`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://auth.calendly.com/oauth/token.

[Official authentication documentation](https://developer.calendly.com/api-docs/3cefb59b832eb-calendly-o-auth-2-0)

### Personal Access Token

Calendly Personal Access Token for private/internal account access

### Credentials

- **API Key:** `apiKey` · required
- **Webhook Signing Key:** `webhookSigningKey` · optional · Optional Calendly webhook signing key for validating webhook payload signatures.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.calendly.com/how-to-authenticate-with-personal-access-tokens)

## Pagination

Use `count` in the query string to set the page size. Use `page_token` in the query string as the pagination cursor.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Sorting

Set the sort field with `sort` in the query string. Only one sort field is accepted.

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Event](actions/cancel-event.md) | `POST /scheduled_events/:event_uuid/cancellation` | [docs](https://developer.calendly.com/api-docs/afb2e9fe3a0a0-cancel-event) |
| [Create Event Invitee](actions/create-event-invitee.md) | `POST /invitees` | [docs](https://developer.calendly.com/api-docs/p3ghrxrwbl8kqe-create-event-invitee) |
| [Create Invitee No Show](actions/create-invitee-no-show.md) | `POST /invitee_no_shows` | [docs](https://developer.calendly.com/api-docs/cebd8c3170790-create-invitee-no-show) |
| [Create One-Off Event Type](actions/create-one-off-event-type.md) | `POST /one_off_event_types` | [docs](https://developer.calendly.com/api-docs/v1yuxil3cpmxq-create-one-off-event-type) |
| [Create Single-Use Scheduling Link](actions/create-single-use-scheduling-link.md) | `POST /scheduling_links` | [docs](https://developer.calendly.com/api-docs/4b8195084e287-create-single-use-scheduling-link) |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | `POST /webhook_subscriptions` | [docs](https://developer.calendly.com/receive-data-from-scheduled-events-in-real-time-with-webhook-subscriptions) |
| [Delete Webhook Subscription](actions/delete-webhook-subscription.md) | `DELETE /webhook_subscriptions/:webhook_uuid` | [docs](https://developer.calendly.com/receive-data-from-scheduled-events-in-real-time-with-webhook-subscriptions) |
| [Get Current User](actions/get-current-user.md) | `GET /users/me` | [docs](https://developer.calendly.com/how-to-find-the-organization-or-user-uri) |
| [Get Event Invitee](actions/get-event-invitee.md) | `GET /scheduled_events/:event_uuid/invitees/:invitee_uuid` | [docs](https://developer.calendly.com/update-your-system-with-data-from-scheduled-events-admins-only) |
| [Get Event Type](actions/get-event-type.md) | `GET /event_types/:event_type_uuid` | [docs](https://developer.calendly.com/how-to-get-scheduling-page-links-for-team-members-across-the-organization) |
| [Get Invitee No Show](actions/get-invitee-no-show.md) | `GET /invitee_no_shows/:invitee_no_show_uuid` | [docs](https://developer.calendly.com/api-docs) |
| [Get Routing Form](actions/get-routing-form.md) | `GET /routing_forms/:routing_form_uuid` | [docs](https://developer.calendly.com/api-docs/20e016678903c-routing-form) |
| [Get Scheduled Event](actions/get-scheduled-event.md) | `GET /scheduled_events/:event_uuid` | [docs](https://developer.calendly.com/update-your-system-with-data-from-scheduled-events-admins-only) |
| [Get Webhook Subscription](actions/get-webhook-subscription.md) | `GET /webhook_subscriptions/:webhook_uuid` | [docs](https://developer.calendly.com/api-docs/4d800dc2cb119-get-webhook-subscription) |
| [List Event Invitees](actions/list-event-invitees.md) | `GET /scheduled_events/:event_uuid/invitees` | [docs](https://developer.calendly.com/update-your-system-with-data-from-scheduled-events-admins-only) |
| [List Event Type Available Times](actions/list-event-type-available-times.md) | `GET /event_type_available_times` | [docs](https://developer.calendly.com/view-event-type-and-user-calendar-availability-data) |
| [List Event Types](actions/list-event-types.md) | `GET /event_types` | [docs](https://developer.calendly.com/how-to-get-scheduling-page-links-for-team-members-across-the-organization) |
| [List Organization Memberships](actions/list-organization-memberships.md) | `GET /organization_memberships` | [docs](https://developer.calendly.com/how-to-find-the-organization-or-user-uri) |
| [List Routing Form Submissions](actions/list-routing-form-submissions.md) | `GET /routing_form_submissions` | [docs](https://developer.calendly.com/api-docs) |
| [List Routing Forms](actions/list-routing-forms.md) | `GET /routing_forms` | [docs](https://developer.calendly.com/api-docs/9fe7334bec6ad-list-routing-forms) |
| [List Scheduled Events](actions/list-scheduled-events.md) | `GET /scheduled_events` | [docs](https://developer.calendly.com/update-your-system-with-data-from-scheduled-events-admins-only) |
| [List User Availability Schedules](actions/list-user-availability-schedules.md) | `GET /user_availability_schedules` | [docs](https://developer.calendly.com/view-event-type-and-user-calendar-availability-data) |
| [List User Busy Times](actions/list-user-busy-times.md) | `GET /user_busy_times` | [docs](https://developer.calendly.com/view-event-type-and-user-calendar-availability-data) |
| [List Webhook Subscriptions](actions/list-webhook-subscriptions.md) | `GET /webhook_subscriptions` | [docs](https://developer.calendly.com/receive-data-from-scheduled-events-in-real-time-with-webhook-subscriptions) |
| [Submit Routing Form](actions/submit-routing-form.md) | `POST /routing_forms/submit` | [docs](https://developer.calendly.com/api-docs) |
| [Unmark Invitee No Show](actions/unmark-invitee-no-show.md) | `DELETE /invitee_no_shows/:invitee_no_show_uuid` | [docs](https://developer.calendly.com/api-docs) |
