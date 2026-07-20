# Let's Calendar: Native API Reference

A consolidated summary of Let's Calendar's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://panel.letscalendar.com/docs
- **API base URL:** `https://panel.letscalendar.com/api/lc`

## Authentication

### OAuth2 M2M Client Key and Secret

Use your Let's Calendar client key and secret key to obtain bearer access tokens.

### Credentials

- **Client Key:** `clientKey` · required · The API client key from your Let's Calendar dashboard.
- **Secret Key:** `secretKey` · required · The API secret key from your Let's Calendar dashboard.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://panel.letscalendar.com/api/lc/access_token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://panel.letscalendar.com/docs)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 50; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Multiple Contacts to Campaign](actions/add-multiple-contacts-to-campaign.md) | `POST add-contacts` | [docs](https://panel.letscalendar.com/docs#apis-POSTapi-lc-add-contacts) |
| [Add Single Contact to Campaign](actions/add-single-contact-to-campaign.md) | `POST add-single-contact` | [docs](https://panel.letscalendar.com/docs#apis-POSTapi-lc-add-single-contact) |
| [Cancel Scheduled Invites](actions/cancel-scheduled-invites.md) | `POST cancel-scheduled-invite` | [docs](https://panel.letscalendar.com/docs#apis-POSTapi-lc-cancel-scheduled-invite) |
| [Create Campaign](actions/create-campaign.md) | `POST create-campaign` | [docs](https://panel.letscalendar.com/docs#apis-POSTapi-lc-create-campaign) |
| [Export Campaign Contacts](actions/export-campaign-contacts.md) | `GET campaign/:campaignId/export-contacts` | [docs](https://panel.letscalendar.com/docs#apis-GETapi-lc-campaign--campaign_id--export-contacts) |
| [Get Campaign Details](actions/get-campaign-details.md) | `GET campaign/:campaignId/edit` | [docs](https://panel.letscalendar.com/docs#apis-GETapi-lc-campaign--campaign_id--edit) |
| [List Campaign Attendees](actions/list-campaign-attendees.md) | `GET campaign/:campaignId/attendees` | [docs](https://panel.letscalendar.com/docs#apis-GETapi-lc-campaign--campaign_id--attendees) |
| [List Campaigns](actions/list-campaigns.md) | `GET campaigns` | [docs](https://panel.letscalendar.com/docs#apis-GETapi-lc-campaigns) |
| [List Senders](actions/list-senders.md) | `GET sender-emails` | [docs](https://panel.letscalendar.com/docs#apis-GETapi-lc-sender-emails) |
| [List Timezones](actions/list-timezones.md) | `GET timezone-list` | [docs](https://panel.letscalendar.com/docs#apis-GETapi-lc-timezone-list) |
| [Schedule Calendar Invites](actions/schedule-calendar-invites.md) | `POST schedule-invite` | [docs](https://panel.letscalendar.com/docs#apis-POSTapi-lc-schedule-invite) |
| [Send Calendar Invites](actions/send-calendar-invites.md) | `POST send-invite` | [docs](https://panel.letscalendar.com/docs#apis-POSTapi-lc-send-invite) |
| [Stop Campaign](actions/stop-campaign.md) | `POST stop-campaign` | [docs](https://panel.letscalendar.com/docs#apis-POSTapi-lc-stop-campaign) |
| [Toggle Campaign Automation Status](actions/toggle-campaign-automation-status.md) | `POST toggle-automation` | [docs](https://panel.letscalendar.com/docs#apis-POSTapi-lc-toggle-automation) |
| [Update Campaign](actions/update-campaign.md) | `PUT campaign/:campaignId` | [docs](https://panel.letscalendar.com/docs#apis-PUTapi-lc-campaign--campaign_id-) |
| [Update Campaign Invites](actions/update-campaign-invites.md) | `POST update-invite` | [docs](https://panel.letscalendar.com/docs#apis-POSTapi-lc-update-invite) |
| [Upload Campaign Contacts](actions/upload-campaign-contacts.md) | `POST upload-contacts` | [docs](https://panel.letscalendar.com/docs#apis-POSTapi-lc-upload-contacts) |
