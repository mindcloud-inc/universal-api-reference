# Resource Guru: Native API Reference

A consolidated summary of Resource Guru's API configuration and 52 documented operations, with links to official documentation.

- **Official docs:** https://resourceguruapp.com/docs/api
- **OpenAPI specification:** https://resourceguruapp.com/docs/api
- **API base URL:** `https://api.resourceguruapp.com/v1/{accountId}`

## Authentication

### OAuth 2.0

Use a Resource Guru OAuth2 application and authorize access to a specific account.

### Credentials

- **Account ID:** `accountId` · required · Resource Guru account URL ID used in request paths, for example mindcloud.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://api.resourceguruapp.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.resourceguruapp.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.resourceguruapp.com/oauth/token.

[Official authentication documentation](https://resourceguruapp.com/docs/api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (52 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Booking](actions/create-booking.md) | `POST /bookings` | [docs](https://resourceguruapp.com/docs/api) |
| [Create Client](actions/create-client.md) | `POST /clients` | [docs](https://resourceguruapp.com/docs/api) |
| [Create Custom Field](actions/create-custom-field.md) | `POST /custom_fields` | [docs](https://resourceguruapp.com/docs/api) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://resourceguruapp.com/docs/api) |
| [Create Resource](actions/create-resource.md) | `POST /resources` | [docs](https://resourceguruapp.com/docs/api) |
| [Create Timesheet](actions/create-timesheet.md) | `POST /timesheets` | [docs](https://resourceguruapp.com/docs/api) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://resourceguruapp.com/docs/api) |
| [Delete Booking](actions/delete-booking.md) | `DELETE /bookings/:id` | [docs](https://resourceguruapp.com/docs/api) |
| [Delete Client](actions/delete-client.md) | `DELETE /clients/:id` | [docs](https://resourceguruapp.com/docs/api) |
| [Delete Custom Field](actions/delete-custom-field.md) | `DELETE /custom_fields/:id` | [docs](https://resourceguruapp.com/docs/api) |
| [Delete Project](actions/delete-project.md) | `DELETE /projects/:id` | [docs](https://resourceguruapp.com/docs/api) |
| [Delete Resource](actions/delete-resource.md) | `DELETE /resources/:id` | [docs](https://resourceguruapp.com/docs/api) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/:id` | [docs](https://resourceguruapp.com/docs/api) |
| [Dismiss Timesheet](actions/dismiss-timesheet.md) | `POST /timesheets/:id/dismiss` | [docs](https://resourceguruapp.com/docs/api) |
| [Get Booking](actions/get-booking.md) | `GET /bookings/:id` | [docs](https://resourceguruapp.com/docs/api) |
| [Get Client](actions/get-client.md) | `GET /clients/:id` | [docs](https://resourceguruapp.com/docs/api) |
| [Get Current User](actions/get-current-user.md) | `GET /users/me` | [docs](https://resourceguruapp.com/docs/api) |
| [Get Custom Field](actions/get-custom-field.md) | `GET /custom_fields/:id` | [docs](https://resourceguruapp.com/docs/api) |
| [Get Project](actions/get-project.md) | `GET /projects/:id` | [docs](https://resourceguruapp.com/docs/api) |
| [Get Resource](actions/get-resource.md) | `GET /resources/:id` | [docs](https://resourceguruapp.com/docs/api) |
| [Get Resource Type](actions/get-resource-type.md) | `GET /resource_types/:id` | [docs](https://resourceguruapp.com/docs/api) |
| [Get User](actions/get-user.md) | `GET /users/{id}` | [docs](https://resourceguruapp.com/docs/api) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhooks/:id` | [docs](https://resourceguruapp.com/docs/api) |
| [Invite Resource](actions/invite-resource.md) | `POST /resources/:id/invite` | [docs](https://resourceguruapp.com/docs/api) |
| [List Activity Types](actions/list-activity-types.md) | `GET /activity_types` | [docs](https://resourceguruapp.com/docs/api) |
| [List Archived Clients](actions/list-archived-clients.md) | `GET /clients/archived` | [docs](https://resourceguruapp.com/docs/api) |
| [List Archived Projects](actions/list-archived-projects.md) | `GET /projects/archived` | [docs](https://resourceguruapp.com/docs/api) |
| [List Archived Resources](actions/list-archived-resources.md) | `GET /resources/archived` | [docs](https://resourceguruapp.com/docs/api) |
| [List Booking Activities](actions/list-booking-activities.md) | `GET /bookings/:id/activities` | [docs](https://resourceguruapp.com/docs/api) |
| [List Bookings](actions/list-bookings.md) | `GET /bookings` | [docs](https://resourceguruapp.com/docs/api) |
| [List Client Bookings](actions/list-client-bookings.md) | `GET /clients/:id/bookings` | [docs](https://resourceguruapp.com/docs/api) |
| [List Clients](actions/list-clients.md) | `GET /clients` | [docs](https://resourceguruapp.com/docs/api) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /custom_fields` | [docs](https://resourceguruapp.com/docs/api) |
| [List Project Bookings](actions/list-project-bookings.md) | `GET /projects/:id/bookings` | [docs](https://resourceguruapp.com/docs/api) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://resourceguruapp.com/docs/api) |
| [List Resource Bookings](actions/list-resource-bookings.md) | `GET /resources/:id/bookings` | [docs](https://resourceguruapp.com/docs/api) |
| [List Resource Types](actions/list-resource-types.md) | `GET /resource_types` | [docs](https://resourceguruapp.com/docs/api) |
| [List Resources](actions/list-resources.md) | `GET /resources` | [docs](https://resourceguruapp.com/docs/api) |
| [List Timesheets](actions/list-timesheets.md) | `GET /timesheets` | [docs](https://resourceguruapp.com/docs/api) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://resourceguruapp.com/docs/api) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://resourceguruapp.com/docs/api) |
| [Remind Booking](actions/remind-booking.md) | `POST /bookings/:id/remind` | [docs](https://resourceguruapp.com/docs/api) |
| [Resolve Booking](actions/resolve-booking.md) | `POST /bookings/:id/resolve` | [docs](https://resourceguruapp.com/docs/api) |
| [Split Booking](actions/split-booking.md) | `POST /bookings/:id/split` | [docs](https://resourceguruapp.com/docs/api) |
| [Test Webhook](actions/test-webhook.md) | `POST /webhooks/:id/test` | [docs](https://resourceguruapp.com/docs/api) |
| [Update Booking](actions/update-booking.md) | `PUT /bookings/:id` | [docs](https://resourceguruapp.com/docs/api) |
| [Update Client](actions/update-client.md) | `PUT /clients/:id` | [docs](https://resourceguruapp.com/docs/api) |
| [Update Custom Field](actions/update-custom-field.md) | `PUT /custom_fields/:id` | [docs](https://resourceguruapp.com/docs/api) |
| [Update Project](actions/update-project.md) | `PUT /projects/:id` | [docs](https://resourceguruapp.com/docs/api) |
| [Update Resource](actions/update-resource.md) | `PUT /resources/:id` | [docs](https://resourceguruapp.com/docs/api) |
| [Update Timesheet](actions/update-timesheet.md) | `PUT /timesheets/:id` | [docs](https://resourceguruapp.com/docs/api) |
| [Update Webhook](actions/update-webhook.md) | `PUT /webhooks/:id` | [docs](https://resourceguruapp.com/docs/api) |
