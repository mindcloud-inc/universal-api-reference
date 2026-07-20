# Nicereply: Native API Reference

A consolidated summary of Nicereply's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://cdn.nicereply.com/s/api/latest/reference/introduction/
- **API base URL:** `https://api.nicereply.com`

## Authentication

### Basic Auth

Use your Nicereply account email as the username and your API token as the password.

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

[Official authentication documentation](https://cdn.nicereply.com/s/api/latest/reference/getting-started/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `pagination.total_pages`. The current page number is read from `pagination.current_page`.

## Pagination

Use `per_page` in the query string to set the page size (default 10; accepted range 10–10000). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign Response Tags](actions/assign-response-tags.md) | `POST /responses/:responseId/tags/:tagId` | [docs](https://cdn.nicereply.com/s/api/latest/reference/responses/tags/assign/) |
| [Create Feedback Object](actions/create-feedback-object.md) | `POST /feedback-objects` | [docs](https://cdn.nicereply.com/s/api/latest/reference/feedback-objects/create/) |
| [Create Response](actions/create-response.md) | `POST /responses` | [docs](https://cdn.nicereply.com/s/api/latest/reference/responses/create/) |
| [Create Tag](actions/create-tag.md) | `POST /tags` | [docs](https://cdn.nicereply.com/s/api/latest/reference/tags/create/) |
| [Get Customer](actions/get-customer.md) | `GET /customers/:id` | [docs](https://cdn.nicereply.com/s/api/latest/reference/customers/view/) |
| [Get Feedback Object](actions/get-feedback-object.md) | `GET /feedback-objects/:id` | [docs](https://cdn.nicereply.com/s/api/latest/reference/feedback-objects/view/) |
| [Get Feedback Object Group](actions/get-feedback-object-group.md) | `GET /feedback-object-groups/:id` | [docs](https://cdn.nicereply.com/s/api/latest/reference/feedback-object-groups/view/) |
| [Get Rating Values Settings](actions/get-rating-values-settings.md) | `GET /rating-values` | [docs](https://cdn.nicereply.com/s/api/latest/reference/rating-values/settings) |
| [Get Response](actions/get-response.md) | `GET /responses/:id` | [docs](https://cdn.nicereply.com/s/api/latest/reference/responses/view/) |
| [Get Response Issue Status](actions/get-response-issue-status.md) | `GET /responses/:id/issue-status` | [docs](https://cdn.nicereply.com/s/api/latest/reference/responses/issue-status/view/) |
| [Get Response Ticket Link](actions/get-response-ticket-link.md) | `GET /responses/:id/ticket-link` | [docs](https://cdn.nicereply.com/s/api/latest/reference/responses/ticket_link/) |
| [Get Survey](actions/get-survey.md) | `GET /surveys/:id` | [docs](https://cdn.nicereply.com/s/api/latest/reference/surveys/view/) |
| [Get Tag](actions/get-tag.md) | `GET /tags/:id` | [docs](https://cdn.nicereply.com/s/api/latest/reference/tags/view/) |
| [Get User](actions/get-user.md) | `GET /users/:id` | [docs](https://cdn.nicereply.com/s/api/latest/reference/users/view/) |
| [Ignore Response Issue Status](actions/ignore-response-issue-status.md) | `POST /responses/:id/issue-status/ignore` | [docs](https://cdn.nicereply.com/s/api/latest/reference/responses/issue-status/ignore/) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://cdn.nicereply.com/s/api/latest/reference/customers/list/) |
| [List Feedback Object Group Responses](actions/list-feedback-object-group-responses.md) | `GET /feedback-object-groups/:id/responses` | [docs](https://cdn.nicereply.com/s/api/latest/reference/feedback-object-groups/responses/list/) |
| [List Feedback Object Groups](actions/list-feedback-object-groups.md) | `GET /feedback-object-groups` | [docs](https://cdn.nicereply.com/s/api/latest/reference/feedback-object-groups/list/) |
| [List Feedback Object Responses](actions/list-feedback-object-responses.md) | `GET /feedback-objects/:id/responses` | [docs](https://cdn.nicereply.com/s/api/latest/reference/feedback-objects/responses/list/) |
| [List Feedback Objects](actions/list-feedback-objects.md) | `GET /feedback-objects` | [docs](https://cdn.nicereply.com/s/api/latest/reference/feedback-objects/list/) |
| [List Integrations](actions/list-integrations.md) | `GET /integrations` | [docs](https://cdn.nicereply.com/s/api/latest/reference/integrations/list/) |
| [List Responses](actions/list-responses.md) | `GET /responses` | [docs](https://cdn.nicereply.com/s/api/latest/reference/responses/list/) |
| [List Survey Responses](actions/list-survey-responses.md) | `GET /surveys/:id/responses` | [docs](https://cdn.nicereply.com/s/api/latest/reference/surveys/responses/list/) |
| [List Surveys](actions/list-surveys.md) | `GET /surveys` | [docs](https://cdn.nicereply.com/s/api/latest/reference/surveys/list/) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://cdn.nicereply.com/s/api/latest/reference/tags/list/) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://cdn.nicereply.com/s/api/latest/reference/users/list/) |
| [Resolve Response Issue Status](actions/resolve-response-issue-status.md) | `POST /responses/:id/issue-status/resolve` | [docs](https://cdn.nicereply.com/s/api/latest/reference/responses/issue-status/resolve/) |
| [Unassign Response Tags](actions/unassign-response-tags.md) | `DELETE /responses/:responseId/tags/:tagId` | [docs](https://cdn.nicereply.com/s/api/latest/reference/responses/tags/unassign/) |
| [Update Response Feedback Object](actions/update-response-feedback-object.md) | `PUT /responses/:id/feedback-object` | [docs](https://cdn.nicereply.com/s/api/latest/reference/responses/update_feedback_object/) |
| [View Survey Distribution](actions/view-survey-distribution.md) | `GET /surveys/:id/distribution` | [docs](https://cdn.nicereply.com/s/api/latest/reference/surveys/view-distribution/) |
