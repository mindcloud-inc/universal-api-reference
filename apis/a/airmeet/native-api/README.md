# Airmeet: Native API Reference

A consolidated summary of Airmeet's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://help.airmeet.com/support/solutions/articles/82000467794-airmeet-public-api-introduction
- **API base URL:** `https://api-gateway-prod.us.airmeet.com/prod`

## Authentication

### Custom Header Auth

Authenticate to Airmeet with access and secret keys, then use the issued access token on API requests.

### Credentials

- **Access Key:** `accessKey` · required · Airmeet access key from the Integrations > API Access Key section.
- **Secret Key:** `secretKey` · required · Airmeet secret key paired with the same generated access key.
- **Access Token:** `accessToken` · optional · Access token returned by POST /auth. Tokens are valid for 30 days.

Send these headers with each API request:

```http
X-Airmeet-Access-Key: <accessKey>
X-Airmeet-Secret-Key: <secretKey>
X-Airmeet-Access-Token: <accessToken>
```

[Official authentication documentation](https://help.airmeet.com/support/solutions/articles/82000467794-airmeet-public-api-introduction)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Authorized Attendee](actions/add-authorized-attendee.md) | `POST /airmeet/{airmeetId}/attendee` | [docs](https://help.airmeet.com/support/solutions/articles/82000909769-2-manage-registrations-airmeet-public-api) |
| [Add Speaker](actions/add-speaker.md) | `POST /airmeet/{airmeetId}/speaker` | [docs](https://help.airmeet.com/support/solutions/articles/82000909770-3-manage-event-airmeet-public-api) |
| [Block Attendee](actions/block-attendee.md) | `PUT /airmeet/{airmeetId}/attendee/block` | [docs](https://help.airmeet.com/support/solutions/articles/82000909769-2-manage-registrations-airmeet-public-api) |
| [Create Airmeet](actions/create-airmeet.md) | `POST /airmeet` | [docs](https://help.airmeet.com/support/solutions/articles/82000909770-3-manage-event-airmeet-public-api) |
| [Create Booth](actions/create-booth.md) | `POST /airmeet/{airmeetId}/booths` | [docs](https://help.airmeet.com/support/solutions/articles/82000909770-3-manage-event-airmeet-public-api) |
| [Create Session](actions/create-session.md) | `POST /airmeet/{airmeetId}/session` | [docs](https://help.airmeet.com/support/solutions/articles/82000909770-3-manage-event-airmeet-public-api) |
| [Customize Event Landing Page](actions/customize-event-landing-page.md) | `PUT /airmeet/{airmeetId}/landing-page` | [docs](https://help.airmeet.com/support/solutions/articles/82000909770-3-manage-event-airmeet-public-api) |
| [Delete Session](actions/delete-session.md) | `DELETE /airmeet/{airmeetId}/session/{sessionId}` | [docs](https://help.airmeet.com/support/solutions/articles/82000909770-3-manage-event-airmeet-public-api) |
| [Duplicate Event](actions/duplicate-event.md) | `POST /airmeet/{airmeetId}/duplication` | [docs](https://help.airmeet.com/support/solutions/articles/82000909770-3-manage-event-airmeet-public-api) |
| [List Airmeets](actions/list-airmeets.md) | `GET /airmeets` | [docs](https://help.airmeet.com/support/solutions/articles/82000909768-1-event-details-airmeet-public-api) |
| [List Booth Attendees](actions/list-booth-attendees.md) | `GET /airmeet/{airmeetId}/booth/{boothId}/booth-attendance` | [docs](https://help.airmeet.com/support/solutions/articles/82000909768-1-event-details-airmeet-public-api) |
| [List Booths](actions/list-booths.md) | `GET /airmeet/{airmeetId}/booths` | [docs](https://help.airmeet.com/support/solutions/articles/82000909768-1-event-details-airmeet-public-api) |
| [List Custom Registration Fields](actions/list-custom-registration-fields.md) | `GET /airmeet/{airmeetId}/custom-fields` | [docs](https://help.airmeet.com/support/solutions/articles/82000909768-1-event-details-airmeet-public-api) |
| [List Event Attendees](actions/list-event-attendees.md) | `GET /airmeet/{airmeetId}/attendees` | [docs](https://help.airmeet.com/support/solutions/articles/82000909768-1-event-details-airmeet-public-api) |
| [List Event Replay Attendees](actions/list-event-replay-attendees.md) | `GET /airmeet/{airmeetId}/event-replay-attendees` | [docs](https://help.airmeet.com/support/solutions/articles/82000909768-1-event-details-airmeet-public-api) |
| [List Event Series](actions/list-event-series.md) | `GET /event-series` | [docs](https://help.airmeet.com/support/solutions/articles/82000912150-4-manage-event-series-airmeet-public-api) |
| [List Event Tracks](actions/list-event-tracks.md) | `GET /airmeet/{airmeetId}/tracks` | [docs](https://help.airmeet.com/support/solutions/articles/82000909768-1-event-details-airmeet-public-api) |
| [List Events in Series](actions/list-events-in-series.md) | `GET /event-series/{eventSeriesId}/events` | [docs](https://help.airmeet.com/support/solutions/articles/82000912150-4-manage-event-series-airmeet-public-api) |
| [List Participants](actions/list-participants.md) | `GET /airmeet/{airmeetId}/participants` | [docs](https://help.airmeet.com/support/solutions/articles/82000909768-1-event-details-airmeet-public-api) |
| [List Poll Responses](actions/list-poll-responses.md) | `GET /airmeet/{airmeetId}/polls` | [docs](https://help.airmeet.com/support/solutions/articles/82000909768-1-event-details-airmeet-public-api) |
| [List Questions Asked](actions/list-questions-asked.md) | `GET /airmeet/{airmeetId}/questions` | [docs](https://help.airmeet.com/support/solutions/articles/82000909768-1-event-details-airmeet-public-api) |
| [List Registration UTMs](actions/list-registration-ut-ms.md) | `GET /airmeet/{airmeetId}/utms` | [docs](https://help.airmeet.com/support/solutions/articles/82000909768-1-event-details-airmeet-public-api) |
| [List Session Attendees](actions/list-session-attendees.md) | `GET /session/{sessionId}/attendees` | [docs](https://help.airmeet.com/support/solutions/articles/82000909768-1-event-details-airmeet-public-api) |
| [List Session Recordings](actions/list-session-recordings.md) | `GET /airmeet/{airmeetId}/session-recordings` | [docs](https://help.airmeet.com/support/solutions/articles/82000909768-1-event-details-airmeet-public-api) |
| [List Sessions](actions/list-sessions.md) | `GET /airmeet/{airmeetId}/info` | [docs](https://help.airmeet.com/support/solutions/articles/82000909768-1-event-details-airmeet-public-api) |
| [Obtain Access Token](actions/obtain-access-token.md) | `POST /auth` | [docs](https://help.airmeet.com/support/solutions/articles/82000909768-1-event-details-airmeet-public-api) |
| [Unblock Attendee](actions/unblock-attendee.md) | `PUT /airmeet/{airmeetId}/attendee/unblock` | [docs](https://help.airmeet.com/support/solutions/articles/82000909769-2-manage-registrations-airmeet-public-api) |
| [Update Airmeet Status](actions/update-airmeet-status.md) | `POST /airmeet/{airmeetId}/status` | [docs](https://help.airmeet.com/support/solutions/articles/82000909770-3-manage-event-airmeet-public-api) |
