# CalendarHero: Native API Reference

A consolidated summary of CalendarHero's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://api.calendarhero.com/documentation
- **OpenAPI specification:** https://api.calendarhero.com/swagger.json
- **API base URL:** `https://api.calendarhero.com`

## Authentication

### API Token

Use a CalendarHero user API token from the CalendarHero settings screen.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.calendarhero.com/documentation)

## API conventions

Response data is read from `data`.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /contact` | [docs](https://api.calendarhero.com/documentation) |
| [Create Directory](actions/create-directory.md) | `POST /user/directories` | [docs](https://api.calendarhero.com/documentation) |
| [Create Meeting Task](actions/create-meeting-task.md) | `POST /meeting/tasks` | [docs](https://api.calendarhero.com/documentation) |
| [Create Meeting Type](actions/create-meeting-type.md) | `POST /user/meeting/{type}` | [docs](https://api.calendarhero.com/documentation) |
| [Create Web Message](actions/create-web-message.md) | `POST /msg/web` | [docs](https://api.calendarhero.com/documentation) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhook/{event}` | [docs](https://api.calendarhero.com/documentation) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contact/{id}` | [docs](https://api.calendarhero.com/documentation) |
| [Delete Directory](actions/delete-directory.md) | `DELETE /user/directories/{uuid}` | [docs](https://api.calendarhero.com/documentation) |
| [Delete Meeting Task](actions/delete-meeting-task.md) | `DELETE /meeting/tasks/{id}` | [docs](https://api.calendarhero.com/documentation) |
| [Delete Meeting Type](actions/delete-meeting-type.md) | `DELETE /user/meeting/{type}` | [docs](https://api.calendarhero.com/documentation) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhook/{event}` | [docs](https://api.calendarhero.com/documentation) |
| [Get Contact](actions/get-contact.md) | `GET /contact/{id}` | [docs](https://api.calendarhero.com/documentation) |
| [Get Contact Count](actions/get-contact-count.md) | `GET /contact/count` | [docs](https://api.calendarhero.com/documentation) |
| [Get Directory](actions/get-directory.md) | `GET /user/directories/{uuid}` | [docs](https://api.calendarhero.com/documentation) |
| [Get Meeting Categories](actions/get-meeting-categories.md) | `GET /meeting/categories` | [docs](https://api.calendarhero.com/documentation) |
| [Get Organization](actions/get-organization.md) | `GET /user/org` | [docs](https://api.calendarhero.com/documentation) |
| [Get Providers](actions/get-providers.md) | `GET /provider` | [docs](https://api.calendarhero.com/documentation) |
| [Get Savings](actions/get-savings.md) | `GET /user/savings` | [docs](https://api.calendarhero.com/documentation) |
| [Get Search Result](actions/get-search-result.md) | `GET /search/{id}` | [docs](https://api.calendarhero.com/documentation) |
| [Get User](actions/get-user.md) | `GET /user` | [docs](https://api.calendarhero.com/documentation) |
| [Get Web Message](actions/get-web-message.md) | `GET /msg/web` | [docs](https://api.calendarhero.com/documentation) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhook/{event}` | [docs](https://api.calendarhero.com/documentation) |
| [Get Webhook Sample](actions/get-webhook-sample.md) | `GET /webhook/{event}/sample` | [docs](https://api.calendarhero.com/documentation) |
| [Import Calendly Event Types](actions/import-calendly-event-types.md) | `GET /user/calendly` | [docs](https://api.calendarhero.com/documentation) |
| [List Directories](actions/list-directories.md) | `GET /user/directories` | [docs](https://api.calendarhero.com/documentation) |
| [List Meeting Tasks](actions/list-meeting-tasks.md) | `GET /meeting/tasks` | [docs](https://api.calendarhero.com/documentation) |
| [List Meeting Types](actions/list-meeting-types.md) | `GET /user/meeting` | [docs](https://api.calendarhero.com/documentation) |
| [List Meetings](actions/list-meetings.md) | `GET /meeting` | [docs](https://api.calendarhero.com/documentation) |
| [Remind Meeting Task](actions/remind-meeting-task.md) | `PUT /meeting/tasks/{id}/remind` | [docs](https://api.calendarhero.com/documentation) |
| [Search Contacts](actions/search-contacts.md) | `GET /contact` | [docs](https://api.calendarhero.com/documentation) |
| [Search Integrations](actions/search-integrations.md) | `GET /search` | [docs](https://api.calendarhero.com/documentation) |
| [Share Meeting Type](actions/share-meeting-type.md) | `POST /user/meeting/{type}/share` | [docs](https://api.calendarhero.com/documentation) |
| [Update Address](actions/update-address.md) | `PUT /user/settings/address` | [docs](https://api.calendarhero.com/documentation) |
| [Update Contact](actions/update-contact.md) | `PUT /contact/{id}` | [docs](https://api.calendarhero.com/documentation) |
| [Update Directory](actions/update-directory.md) | `PUT /user/directories/{uuid}` | [docs](https://api.calendarhero.com/documentation) |
| [Update Meeting Type](actions/update-meeting-type.md) | `PUT /user/meeting` | [docs](https://api.calendarhero.com/documentation) |
| [Update Restricted Apps](actions/update-restricted-apps.md) | `PUT /user/settings/restrictedapps` | [docs](https://api.calendarhero.com/documentation) |
| [Update User](actions/update-user.md) | `PUT /user` | [docs](https://api.calendarhero.com/documentation) |
| [Update User Info](actions/update-user-info.md) | `PUT /user/settings/info` | [docs](https://api.calendarhero.com/documentation) |
| [Update Work Location](actions/update-work-location.md) | `PUT /user/settings/worklocation` | [docs](https://api.calendarhero.com/documentation) |
