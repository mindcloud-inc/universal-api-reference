# ECAL: Native API Reference

A consolidated summary of ECAL's API configuration and 29 documented operations, with links to official documentation.

- **Official docs:** https://docs.ecal.com/reference/apiv2.html
- **API base URL:** `https://api.ecal.com/apiv2`

## Authentication

### API Key + Secret

Sign ECAL APIv2 requests with the API Key and associated API Secret.

### Credentials

- **API Key:** `apiKey` · required
- **API Secret:** `apiSecret` · required · The API Secret associated with the ECAL API Key. Used only to generate the apiSign query parameter; it is never sent as a request parameter.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.ecal.com/reference/apiv2/authentication.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (29 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Subscriber Subscriptions](actions/add-subscriber-subscriptions.md) | `POST /subscriber/:ecalId/subscriptions/add` | [docs](https://docs.ecal.com/reference/apiv2/subscriber.html#post-apiv2subscriberidsubscriptionsadd) |
| [Bulk Update Events By Reference Type](actions/bulk-update-events-by-reference-type.md) | `PUT /events/:referenceType` | [docs](https://docs.ecal.com/reference/apiv2/event.html#put-apiv2eventsreferencetype) |
| [Create Account](actions/create-account.md) | `POST /account` | [docs](https://docs.ecal.com/reference/apiv2/account.html) |
| [Create Batch Private Events](actions/create-batch-private-events.md) | `POST /batch/events` | [docs](https://docs.ecal.com/reference/private/batch.html#adding-private-batch-events) |
| [Create Calendar](actions/create-calendar.md) | `POST /calendar/` | [docs](https://docs.ecal.com/reference/apiv2/calendar.html#post-apiv2calendar) |
| [Create Event](actions/create-event.md) | `POST /event/` | [docs](https://docs.ecal.com/reference/apiv2/event.html#post-apiv2event) |
| [Create Private Event](actions/create-private-event.md) | `POST /event/` | [docs](https://docs.ecal.com/reference/private/single.html#post-private-events) |
| [Delete Batch Private Events](actions/delete-batch-private-events.md) | `DELETE /batch/events` | [docs](https://docs.ecal.com/reference/private/batch.html#deleting-private-events) |
| [Delete Calendar](actions/delete-calendar.md) | `DELETE /calendar/:calendarId` | [docs](https://docs.ecal.com/reference/apiv2/calendar.html#delete-apiv2calendarid) |
| [Delete Event](actions/delete-event.md) | `DELETE /event/:eventIdOrReference` | [docs](https://docs.ecal.com/reference/apiv2/event.html#delete-apiv2eventid) |
| [Delete Private Event](actions/delete-private-event.md) | `DELETE /event/:eventIdOrReference` | [docs](https://docs.ecal.com/reference/private/single.html#delete-private-events) |
| [Get Calendar](actions/get-calendar.md) | `GET /calendar/:calendarId` | [docs](https://docs.ecal.com/reference/apiv2/calendar.html#get-apiv2calendarid) |
| [Get Calendar By Reference](actions/get-calendar-by-reference.md) | `GET /calendar/:reference` | [docs](https://docs.ecal.com/reference/apiv2/calendar.html#get-apiv2calendarreference) |
| [Get Event](actions/get-event.md) | `GET /event/:eventId` | [docs](https://docs.ecal.com/reference/apiv2/event.html#get-apiv2eventid) |
| [Get Subscriber By ECAL ID](actions/get-subscriber-by-ecal-id.md) | `GET /subscriber/:ecalId` | [docs](https://docs.ecal.com/reference/apiv2/subscriber.html) |
| [Get Subscriber By Email](actions/get-subscriber-by-email.md) | `GET /subscriber/:emailAddress` | [docs](https://docs.ecal.com/reference/apiv2/subscriber.html) |
| [List Accounts](actions/list-accounts.md) | `GET /account` | [docs](https://docs.ecal.com/reference/apiv2/account.html) |
| [List Batch Private Events By Reference Type](actions/list-batch-private-events-by-reference-type.md) | `GET /batch/events` | [docs](https://docs.ecal.com/reference/private/batch.html#retrieving-events-by-reference-type) |
| [List Batch Private Events By Subscriber](actions/list-batch-private-events-by-subscriber.md) | `GET /batch/events` | [docs](https://docs.ecal.com/reference/private/batch.html#retrieving-events-by-subscriber-id) |
| [List Batch Private Events By Subscriber And Reference Type](actions/list-batch-private-events-by-subscriber-and-reference-type.md) | `GET /batch/events` | [docs](https://docs.ecal.com/reference/private/batch.html#retrieving-events-by-subscriber-id-and-reference-type) |
| [List Calendars](actions/list-calendars.md) | `GET /calendar/` | [docs](https://docs.ecal.com/reference/apiv2/calendar.html) |
| [List Events](actions/list-events.md) | `GET /event/` | [docs](https://docs.ecal.com/reference/apiv2/event.html#get-apiv2event) |
| [List Private Events](actions/list-private-events.md) | `GET /event/` | [docs](https://docs.ecal.com/reference/private/single.html#get-private-events) |
| [Remove Subscriber Subscriptions](actions/remove-subscriber-subscriptions.md) | `POST /subscriber/:ecalId/subscriptions/remove` | [docs](https://docs.ecal.com/reference/apiv2/subscriber.html#post-apiv2subscriberidsubscriptionsremove) |
| [Search Batch Private Events By IDs](actions/search-batch-private-events-by-ids.md) | `POST /batch/events/search` | [docs](https://docs.ecal.com/reference/private/batch.html#retrieving-events-by-list-of-events-ids) |
| [Unsubscribe Subscriber](actions/unsubscribe-subscriber.md) | `POST /subscriber/:ecalId/unsubscribe` | [docs](https://docs.ecal.com/reference/apiv2/subscriber.html#post-apiv2subscriberidunsubscribe) |
| [Update Calendar](actions/update-calendar.md) | `PUT /calendar/:calendarId` | [docs](https://docs.ecal.com/reference/apiv2/calendar.html#put-apiv2calendarid) |
| [Update Event](actions/update-event.md) | `PUT /event/:eventIdOrReference` | [docs](https://docs.ecal.com/reference/apiv2/event.html#put-apiv2eventid) |
| [Update Private Event](actions/update-private-event.md) | `PUT /event/:eventIdOrReference` | [docs](https://docs.ecal.com/reference/private/single.html#put-private-events) |
