# Close: Native API Reference

A consolidated summary of Close's API configuration and 41 documented operations, with links to official documentation.

- **Official docs:** https://developer.close.com/
- **API base URL:** `https://api.close.com/api/v1`

## Authentication

### Basic Auth

HTTP Basic authentication for Close API using the API key as the username and a blank password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://developer.close.com/api/overview/api-key-authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `_limit` in the query string to set the page size (default 100). Use `_skip` in the query string as the record offset; numbering starts at 0.

## Endpoints (41 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /contact/` | [docs](https://developer.close.com/resources/contacts/) |
| [Create Lead](actions/create-lead.md) | `POST /lead/` | [docs](https://developer.close.com/resources/leads/) |
| [Create Opportunity](actions/create-opportunity.md) | `POST /opportunity/` | [docs](https://developer.close.com/resources/opportunities/) |
| [Create Smart View](actions/create-smart-view.md) | `POST /saved_search/` | [docs](https://developer.close.com/resources/smart-views/) |
| [Create Task](actions/create-task.md) | `POST /task/` | [docs](https://developer.close.com/resources/tasks/) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contact/:id/` | [docs](https://developer.close.com/resources/contacts/) |
| [Delete Lead](actions/delete-lead.md) | `DELETE /lead/:id/` | [docs](https://developer.close.com/resources/leads/) |
| [Delete Opportunity](actions/delete-opportunity.md) | `DELETE /opportunity/:id/` | [docs](https://developer.close.com/resources/opportunities/) |
| [Delete Smart View](actions/delete-smart-view.md) | `DELETE /saved_search/:id/` | [docs](https://developer.close.com/resources/smart-views/) |
| [Delete Task](actions/delete-task.md) | `DELETE /task/:id/` | [docs](https://developer.close.com/resources/tasks/) |
| [Get Contact](actions/get-contact.md) | `GET /contact/:id/` | [docs](https://developer.close.com/resources/contacts/) |
| [Get Current User](actions/get-current-user.md) | `GET /me/` | [docs](https://developer.close.com/resources/users/) |
| [Get Email Template](actions/get-email-template.md) | `GET /email_template/:id/` | [docs](https://developer.close.com/resources/email-templates/) |
| [Get Lead](actions/get-lead.md) | `GET /lead/:id/` | [docs](https://developer.close.com/resources/leads/) |
| [Get Opportunity](actions/get-opportunity.md) | `GET /opportunity/:id/` | [docs](https://developer.close.com/resources/opportunities/) |
| [Get Smart View](actions/get-smart-view.md) | `GET /saved_search/:id/` | [docs](https://developer.close.com/resources/smart-views/) |
| [Get SMS Template](actions/get-sms-template.md) | `GET /sms_template/:id/` | [docs](https://developer.close.com/resources/sms-templates/) |
| [Get Task](actions/get-task.md) | `GET /task/:id/` | [docs](https://developer.close.com/resources/tasks/) |
| [Get User](actions/get-user.md) | `GET /user/:id/` | [docs](https://developer.close.com/resources/users/) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhook/:id/` | [docs](https://developer.close.com/resources/webhooks/) |
| [List Activities](actions/list-activities.md) | `GET /activity/` | [docs](https://developer.close.com/resources/activities/) |
| [List Contacts](actions/list-contacts.md) | `GET /contact/` | [docs](https://developer.close.com/resources/contacts/) |
| [List Email Templates](actions/list-email-templates.md) | `GET /email_template/` | [docs](https://developer.close.com/resources/email-templates/) |
| [List Lead Statuses](actions/list-lead-statuses.md) | `GET /status/lead/` | [docs](https://developer.close.com/resources/lead-statuses/) |
| [List Leads](actions/list-leads.md) | `GET /lead/` | [docs](https://developer.close.com/resources/leads/) |
| [List Opportunities](actions/list-opportunities.md) | `GET /opportunity/` | [docs](https://developer.close.com/resources/opportunities/) |
| [List Opportunity Statuses](actions/list-opportunity-statuses.md) | `GET /status/opportunity/` | [docs](https://developer.close.com/resources/opportunity-statuses/) |
| [List Pipelines](actions/list-pipelines.md) | `GET /pipeline/` | [docs](https://developer.close.com/resources/pipelines/) |
| [List Sequences](actions/list-sequences.md) | `GET /sequence/` | [docs](https://developer.close.com/resources/sequences/) |
| [List Smart Views](actions/list-smart-views.md) | `GET /saved_search/` | [docs](https://developer.close.com/resources/smart-views/) |
| [List SMS Templates](actions/list-sms-templates.md) | `GET /sms_template/` | [docs](https://developer.close.com/resources/sms-templates/) |
| [List Tasks](actions/list-tasks.md) | `GET /task/` | [docs](https://developer.close.com/resources/tasks/) |
| [List User Availabilities](actions/list-user-availabilities.md) | `GET /user/availability/` | [docs](https://developer.close.com/resources/users/) |
| [List Users](actions/list-users.md) | `GET /user/` | [docs](https://developer.close.com/resources/users/) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhook/` | [docs](https://developer.close.com/resources/webhooks/) |
| [Merge Leads](actions/merge-leads.md) | `POST /lead/merge/` | [docs](https://developer.close.com/resources/leads/) |
| [Update Contact](actions/update-contact.md) | `PUT /contact/:id/` | [docs](https://developer.close.com/resources/contacts/) |
| [Update Lead](actions/update-lead.md) | `PUT /lead/:id/` | [docs](https://developer.close.com/resources/leads/) |
| [Update Opportunity](actions/update-opportunity.md) | `PUT /opportunity/:id/` | [docs](https://developer.close.com/resources/opportunities/) |
| [Update Smart View](actions/update-smart-view.md) | `PUT /saved_search/:id/` | [docs](https://developer.close.com/resources/smart-views/) |
| [Update Task](actions/update-task.md) | `PUT /task/:id/` | [docs](https://developer.close.com/resources/tasks/) |
