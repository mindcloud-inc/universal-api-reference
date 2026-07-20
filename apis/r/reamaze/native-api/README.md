# Reamaze: Native API Reference

A consolidated summary of Reamaze's API configuration and 38 documented operations, with links to official documentation.

- **Official docs:** https://www.reamaze.com/api
- **API base URL:** `https://{brand}.reamaze.io/api/v1`

## Authentication

### Basic Auth

Authenticate with your Reamaze login email and API token over HTTP Basic Auth.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **Brand:** `brand` · required · Your Reamaze brand slug. If your account URL is https://mindcloud.reamaze.com, use mindcloud.

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://www.reamaze.com/api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (38 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Article](actions/create-article.md) | `POST /topics/:slug/articles` | [docs](https://www.reamaze.com/api/post_article) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://www.reamaze.com/api/post_contacts) |
| [Create Contact Note](actions/create-contact-note.md) | `POST /contacts/:contactIdentifier/notes` | [docs](https://www.reamaze.com/api/post_notes) |
| [Create Conversation](actions/create-conversation.md) | `POST /conversations` | [docs](https://www.reamaze.com/api/post_conversations) |
| [Create Identity](actions/create-identity.md) | `POST /contacts/:email/identities` | [docs](https://www.reamaze.com/api/post_identities) |
| [Create Incident](actions/create-incident.md) | `POST /incidents` | [docs](https://www.reamaze.com/api/post_incident) |
| [Create Message](actions/create-message.md) | `POST /conversations/:slug/messages` | [docs](https://www.reamaze.com/api/post_messages) |
| [Create Response Template](actions/create-response-template.md) | `POST /response_templates` | [docs](https://www.reamaze.com/api/post_response_template) |
| [Create Staff](actions/create-staff.md) | `POST /staff` | [docs](https://www.reamaze.com/api/post_staff) |
| [Delete Contact Note](actions/delete-contact-note.md) | `DELETE /contacts/:contactIdentifier/notes/:id` | [docs](https://www.reamaze.com/api/delete_note) |
| [Get Article](actions/get-article.md) | `GET /articles/:slug` | [docs](https://www.reamaze.com/api/get_article) |
| [Get Channel](actions/get-channel.md) | `GET /channels/:slug` | [docs](https://www.reamaze.com/api/get_channel) |
| [Get Channel Summary Report](actions/get-channel-summary-report.md) | `GET /reports/channel_summary` | [docs](https://www.reamaze.com/api/get_reports_channel_summary) |
| [Get Conversation](actions/get-conversation.md) | `GET /conversations/:slug` | [docs](https://www.reamaze.com/api/get_conversation) |
| [Get Incident](actions/get-incident.md) | `GET /incidents/:identifier` | [docs](https://www.reamaze.com/api/get_incident) |
| [Get Response Template](actions/get-response-template.md) | `GET /response_templates/:id` | [docs](https://www.reamaze.com/api/get_response_template) |
| [Get Response Time Report](actions/get-response-time-report.md) | `GET /reports/response_time` | [docs](https://www.reamaze.com/api/get_reports_response_time) |
| [Get Staff Report](actions/get-staff-report.md) | `GET /reports/staff` | [docs](https://www.reamaze.com/api/get_reports_staff) |
| [Get Tags Report](actions/get-tags-report.md) | `GET /reports/tags` | [docs](https://www.reamaze.com/api/get_reports_tags) |
| [Get Volume Report](actions/get-volume-report.md) | `GET /reports/volume` | [docs](https://www.reamaze.com/api/get_reports_volume) |
| [List Articles](actions/list-articles.md) | `GET /articles` | [docs](https://www.reamaze.com/api/get_articles) |
| [List Channels](actions/list-channels.md) | `GET /channels` | [docs](https://www.reamaze.com/api/get_channels) |
| [List Contact Identities](actions/list-contact-identities.md) | `GET /contacts/:email/identities` | [docs](https://www.reamaze.com/api/get_identities) |
| [List Contact Notes](actions/list-contact-notes.md) | `GET /contacts/:contactIdentifier/notes` | [docs](https://www.reamaze.com/api/get_notes) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://www.reamaze.com/api/get_contacts) |
| [List Conversations](actions/list-conversations.md) | `GET /conversations` | [docs](https://www.reamaze.com/api/get_conversations) |
| [List Incidents](actions/list-incidents.md) | `GET /incidents` | [docs](https://www.reamaze.com/api/get_incidents) |
| [List Messages](actions/list-messages.md) | `GET /messages` | [docs](https://www.reamaze.com/api/get_messages) |
| [List Response Templates](actions/list-response-templates.md) | `GET /response_templates` | [docs](https://www.reamaze.com/api/get_response_templates) |
| [List Satisfaction Ratings](actions/list-satisfaction-ratings.md) | `GET /satisfaction_ratings` | [docs](https://www.reamaze.com/api/get_satisfaction_ratings) |
| [List Staff](actions/list-staff.md) | `GET /staff` | [docs](https://www.reamaze.com/api/get_staff) |
| [List Systems](actions/list-systems.md) | `GET /systems` | [docs](https://www.reamaze.com/api/get_systems) |
| [Update Article](actions/update-article.md) | `PUT /articles/:slug` | [docs](https://www.reamaze.com/api/put_article) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/:identifier` | [docs](https://www.reamaze.com/api/put_contacts) |
| [Update Contact Note](actions/update-contact-note.md) | `PUT /contacts/:contactIdentifier/notes/:id` | [docs](https://www.reamaze.com/api/put_note) |
| [Update Conversation](actions/update-conversation.md) | `PUT /conversations/:slug` | [docs](https://www.reamaze.com/api/put_conversations) |
| [Update Incident](actions/update-incident.md) | `PUT /incidents/:identifier` | [docs](https://www.reamaze.com/api/put_incident) |
| [Update Response Template](actions/update-response-template.md) | `PUT /response_templates/:slug` | [docs](https://www.reamaze.com/api/put_response_template) |
