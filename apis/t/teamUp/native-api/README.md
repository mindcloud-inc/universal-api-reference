# TeamUp: Native API Reference

A consolidated summary of TeamUp's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.teamup.com/docs/api/f835b6c908790-teamup-com-api-overview
- **OpenAPI specification:** https://stoplight.io/api/v1/projects/teamup/api/nodes/reference/generated_docs_public.yaml
- **API base URL:** `https://api.teamup.com`

## Authentication

### API Key

Connect with a TeamUp API key plus a TeamUp calendar key for calendar-scoped API calls.

### Credentials

- **API Key:** `apiKey` · required
- **Calendar Key:** `calendarKeyOrId` · required · TeamUp calendar key used in API paths. Use an admin-capable TeamUp calendar key from TeamUp Sharing when possible; the public calendar URL code alone is not sufficient for this apiKey wrapper.

Send these headers with each API request:

```http
Teamup-Token: <apiKey>
```

[Official authentication documentation](https://apidocs.teamup.com/docs/api/e60b71a05cf57-authentication)

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | `POST /:calendarKeyOrId/events` | [docs](https://apidocs.teamup.com/docs/api/3269d0159ae9f-create-an-event) |
| [Delete Event](actions/delete-event.md) | `DELETE /:calendarKeyOrId/events/:eventId` | [docs](https://apidocs.teamup.com/docs/api/260f3631bec7b-delete-an-event) |
| [Get Calendar Configuration](actions/get-calendar-configuration.md) | `GET /:calendarKeyOrId/configuration` | [docs](https://apidocs.teamup.com/docs/api/1e4f067e212e8-get-the-calendar-configuration) |
| [Get Event](actions/get-event.md) | `GET /:calendarKeyOrId/events/:eventId` | [docs](https://apidocs.teamup.com/docs/api/016e0077fd9cc-get-an-event) |
| [Get Event Page URL](actions/get-event-page-url.md) | `POST /:calendarKey/events/:eventId/pointer` | [docs](https://apidocs.teamup.com/docs/api/5d279882e0f60-get-event-page-url) |
| [List Events](actions/list-events.md) | `GET /:calendarKeyOrId/events` | [docs](https://apidocs.teamup.com/docs/api/0f9f896800ffe-get-events) |
| [Update Event](actions/update-event.md) | `PUT /:calendarKeyOrId/events/:eventId` | [docs](https://apidocs.teamup.com/docs/api/8b5d0d1556103-update-an-event) |
