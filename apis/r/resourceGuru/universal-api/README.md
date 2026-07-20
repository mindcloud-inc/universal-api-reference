# <img src="https://images.mindcloud.co/apps/icons/resource-guru-icon_1775664881261.png" alt="Resource Guru logo" width="28" height="28"> Resource Guru: Universal API

Connect Resource Guru to read and manage accounts, resources, bookings, clients, projects, time off, timesheets, custom fields, reports, and webhooks through the official OAuth2 API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/resourceGuru/latest
- **Actions:** 52
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://resourceguruapp.com
- **Vendor API docs:** https://resourceguruapp.com/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Resources](actions/list-resources.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/resourceGuru/latest/actions/list-resources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (52)

### Activity Type

| Action | Method | Description |
| --- | --- | --- |
| [List Activity Types](actions/list-activity-types.md) | GET | Retrieves activity types from Resource Guru. |

### Archived Client

| Action | Method | Description |
| --- | --- | --- |
| [List Archived Clients](actions/list-archived-clients.md) | GET | Retrieves archived clients from Resource Guru. |

### Archived Project

| Action | Method | Description |
| --- | --- | --- |
| [List Archived Projects](actions/list-archived-projects.md) | GET | Retrieves archived projects from Resource Guru. |

### Archived Resource

| Action | Method | Description |
| --- | --- | --- |
| [List Archived Resources](actions/list-archived-resources.md) | GET | Retrieves archived resources from Resource Guru. |

### Booking

| Action | Method | Description |
| --- | --- | --- |
| [Create Booking](actions/create-booking.md) | POST | Creates a new booking in Resource Guru. |
| [Delete Booking](actions/delete-booking.md) | DELETE | Deletes an existing booking from Resource Guru. |
| [Get Booking](actions/get-booking.md) | GET | Retrieves a booking from Resource Guru. |
| [List Bookings](actions/list-bookings.md) | GET | Retrieves bookings from Resource Guru. |
| [Update Booking](actions/update-booking.md) | PUT | Updates an existing booking in Resource Guru. |

### Booking Activity

| Action | Method | Description |
| --- | --- | --- |
| [List Booking Activities](actions/list-booking-activities.md) | GET | Retrieves activities for a booking from Resource Guru. |

### Booking Reminder

| Action | Method | Description |
| --- | --- | --- |
| [Remind Booking](actions/remind-booking.md) | PUT | Sends a booking reminder in Resource Guru. |

### Booking Resolution

| Action | Method | Description |
| --- | --- | --- |
| [Resolve Booking](actions/resolve-booking.md) | PUT | Resolves a booking in Resource Guru. |

### Booking Split

| Action | Method | Description |
| --- | --- | --- |
| [Split Booking](actions/split-booking.md) | PUT | Splits a booking in Resource Guru. |

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST | Creates a new client in Resource Guru. |
| [Delete Client](actions/delete-client.md) | DELETE | Deletes an existing client from Resource Guru. |
| [Get Client](actions/get-client.md) | GET | Retrieves a client from Resource Guru. |
| [List Clients](actions/list-clients.md) | GET | Retrieves clients from Resource Guru. |
| [Update Client](actions/update-client.md) | PUT | Updates an existing client in Resource Guru. |

### Client Booking

| Action | Method | Description |
| --- | --- | --- |
| [List Client Bookings](actions/list-client-bookings.md) | GET | Retrieves bookings for a client from Resource Guru. |

### Current User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Resource Guru. |

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Field](actions/create-custom-field.md) | POST | Creates a new custom field in Resource Guru. |
| [Delete Custom Field](actions/delete-custom-field.md) | DELETE | Deletes an existing custom field from Resource Guru. |
| [Get Custom Field](actions/get-custom-field.md) | GET | Retrieves a custom field from Resource Guru. |
| [List Custom Fields](actions/list-custom-fields.md) | GET | Retrieves custom fields from Resource Guru. |
| [Update Custom Field](actions/update-custom-field.md) | PUT | Updates an existing custom field in Resource Guru. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Resource Guru. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from Resource Guru. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Resource Guru. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Resource Guru. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Resource Guru. |

### Project Booking

| Action | Method | Description |
| --- | --- | --- |
| [List Project Bookings](actions/list-project-bookings.md) | GET | Retrieves bookings for a project from Resource Guru. |

### Resource

| Action | Method | Description |
| --- | --- | --- |
| [Create Resource](actions/create-resource.md) | POST | Creates a new resource in Resource Guru. |
| [Delete Resource](actions/delete-resource.md) | DELETE | Deletes an existing resource from Resource Guru. |
| [Get Resource](actions/get-resource.md) | GET | Retrieves a resource from Resource Guru. |
| [List Resources](actions/list-resources.md) | GET | Retrieves resources from Resource Guru. |
| [Update Resource](actions/update-resource.md) | PUT | Updates an existing resource in Resource Guru. |

### Resource Booking

| Action | Method | Description |
| --- | --- | --- |
| [List Resource Bookings](actions/list-resource-bookings.md) | GET | Retrieves bookings for a resource from Resource Guru. |

### Resource Invitation

| Action | Method | Description |
| --- | --- | --- |
| [Invite Resource](actions/invite-resource.md) | PUT | Invites a resource in Resource Guru. |

### Resource Type

| Action | Method | Description |
| --- | --- | --- |
| [Get Resource Type](actions/get-resource-type.md) | GET | Retrieves a resource type from Resource Guru. |
| [List Resource Types](actions/list-resource-types.md) | GET | Retrieves resource types from Resource Guru. |

### Timesheet

| Action | Method | Description |
| --- | --- | --- |
| [Create Timesheet](actions/create-timesheet.md) | POST | Creates a new timesheet in Resource Guru. |
| [List Timesheets](actions/list-timesheets.md) | GET | Retrieves timesheets from Resource Guru. |
| [Update Timesheet](actions/update-timesheet.md) | PUT | Updates an existing timesheet in Resource Guru. |

### Timesheet Dismissal

| Action | Method | Description |
| --- | --- | --- |
| [Dismiss Timesheet](actions/dismiss-timesheet.md) | PUT | Dismisses a timesheet in Resource Guru. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Resource Guru. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Resource Guru. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Resource Guru. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Resource Guru. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from Resource Guru. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Resource Guru. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Resource Guru. |

### Webhook Test

| Action | Method | Description |
| --- | --- | --- |
| [Test Webhook](actions/test-webhook.md) | PUT | Tests a webhook in Resource Guru. |

