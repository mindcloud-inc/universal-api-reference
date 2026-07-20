# Whattime: Native API Reference

A consolidated summary of Whattime's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developer.whattime.co.kr/swagger
- **OpenAPI specification:** https://developer.whattime.co.kr/swagger.json
- **API base URL:** `https://api.whattime.co.kr/v1`

## Authentication

### API Token

Use a Whattime API token sent as Authorization: Bearer <token>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.whattime.co.kr/swagger)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `pagination.next_page_token`.

## Pagination

Use `page_token` in the query string as the pagination cursor. Follow the complete next-page URL returned by the API.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Schedule](actions/cancel-schedule.md) | `POST /schedules/:code/cancel` | [docs](https://developer.whattime.co.kr/swagger#/Schedule/schedulesCancel) |
| [Create Availability](actions/create-availability.md) | `POST /availabilities` | [docs](https://developer.whattime.co.kr/swagger#/Availability/availabilitiesCreate) |
| [Create Calendar Connection](actions/create-calendar-connection.md) | `POST /connects` | [docs](https://developer.whattime.co.kr/swagger#/Connect/connectsCreate) |
| [Create Routing Form](actions/create-routing-form.md) | `POST /routing_forms` | [docs](https://developer.whattime.co.kr/swagger#/RoutingForm/routingFormsCreate) |
| [Create Schedule](actions/create-schedule.md) | `POST /schedules` | [docs](https://developer.whattime.co.kr/swagger#/Schedule/schedulesCreate) |
| [Create User](actions/create-user.md) | `POST /users` | [docs](https://developer.whattime.co.kr/swagger#/User/usersCreate) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://developer.whattime.co.kr/swagger#/Webhook/webhooksCreate) |
| [Delete Availability](actions/delete-availability.md) | `DELETE /availabilities/:code` | [docs](https://developer.whattime.co.kr/swagger#/Availability/availabilitiesDeleteByCode) |
| [Delete Calendar Connection](actions/delete-calendar-connection.md) | `DELETE /connects/:id` | [docs](https://developer.whattime.co.kr/swagger#/Connect/connectsDeleteByCode) |
| [Delete Organization Member](actions/delete-organization-member.md) | `DELETE /organization_members/:code` | [docs](https://developer.whattime.co.kr/swagger#/Organization/organizationMemberDestroy) |
| [Get Availability](actions/get-availability.md) | `GET /availabilities/:code` | [docs](https://developer.whattime.co.kr/swagger#/Availability/availabilitiesByCode) |
| [Get Basic Availability](actions/get-basic-availability.md) | `GET /availabilities/basic` | [docs](https://developer.whattime.co.kr/swagger#/Availability/availabilitiesBasic) |
| [Get Calendar](actions/get-calendar.md) | `GET /calendars/:code` | [docs](https://developer.whattime.co.kr/swagger#/Calendar/calendarsByCode) |
| [Get Calendar Connection](actions/get-calendar-connection.md) | `GET /connects/:id` | [docs](https://developer.whattime.co.kr/swagger#/Connect/connectsByCode) |
| [Get Current Auth User](actions/get-current-auth-user.md) | `GET /auth/user` | [docs](https://developer.whattime.co.kr/swagger#/Auth/authUser) |
| [Get Current Organization](actions/get-current-organization.md) | `GET /auth/organization` | [docs](https://developer.whattime.co.kr/swagger#/Auth/authOrganization) |
| [Get My User](actions/get-my-user.md) | `GET /users/me` | [docs](https://developer.whattime.co.kr/swagger#/User/usersMe) |
| [Get Organization Member](actions/get-organization-member.md) | `GET /organization_members/:code` | [docs](https://developer.whattime.co.kr/swagger#/Organization/organizationMembersByCode) |
| [Get Reservation](actions/get-reservation.md) | `GET /reservations/:code` | [docs](https://developer.whattime.co.kr/swagger#/Reservation/reservationsByCode) |
| [Get Routing Form](actions/get-routing-form.md) | `GET /routing_forms/:code` | [docs](https://developer.whattime.co.kr/swagger#/RoutingForm/routingFormsByCode) |
| [Get Schedule](actions/get-schedule.md) | `GET /schedules/:code` | [docs](https://developer.whattime.co.kr/swagger#/Schedule/scheduleByCode) |
| [Get User](actions/get-user.md) | `GET /users/:code` | [docs](https://developer.whattime.co.kr/swagger#/User/usersByCode) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhooks/:code` | [docs](https://developer.whattime.co.kr/swagger#/Webhook/webhooksByCode) |
| [Invite Organization Member](actions/invite-organization-member.md) | `POST /organization_members` | [docs](https://developer.whattime.co.kr/swagger#/Organization/organizationMemberCreate) |
| [List Availabilities](actions/list-availabilities.md) | `GET /availabilities` | [docs](https://developer.whattime.co.kr/swagger#/Availability/availabilities) |
| [List Calendar Connections](actions/list-calendar-connections.md) | `GET /connects` | [docs](https://developer.whattime.co.kr/swagger#/Connect/connects) |
| [List Calendar Slots](actions/list-calendar-slots.md) | `GET /reservation/calendars/:code/slots` | [docs](https://developer.whattime.co.kr/swagger#/Calendar/reservationCalendarSlots) |
| [List Calendars](actions/list-calendars.md) | `GET /calendars` | [docs](https://developer.whattime.co.kr/swagger#/Calendar/calendars) |
| [List Organization Members](actions/list-organization-members.md) | `GET /organization_members` | [docs](https://developer.whattime.co.kr/swagger#/Organization/organizationMembers) |
| [List Recent Schedules](actions/list-recent-schedules.md) | `GET /schedules/recent` | [docs](https://developer.whattime.co.kr/swagger#/Schedule/reservationsRecent) |
| [List Reservations](actions/list-reservations.md) | `GET /reservations` | [docs](https://developer.whattime.co.kr/swagger#/Reservation/reservations) |
| [List Routing Forms](actions/list-routing-forms.md) | `GET /routing_forms` | [docs](https://developer.whattime.co.kr/swagger#/RoutingForm/routing_forms) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://developer.whattime.co.kr/swagger#/Webhook/webhooks) |
| [Reschedule Schedule](actions/reschedule-schedule.md) | `POST /schedules/:code/reschedule` | [docs](https://developer.whattime.co.kr/swagger#/Schedule/schedulesReschedule) |
| [Update Availability](actions/update-availability.md) | `PUT /availabilities/:code` | [docs](https://developer.whattime.co.kr/swagger#/Availability/availabilitiesUpdateByCode) |
| [Update Basic Availability](actions/update-basic-availability.md) | `PUT /availabilities/basic` | [docs](https://developer.whattime.co.kr/swagger#/Availability/availabilitiesBasicUpdateByCode) |
| [Update Organization Member](actions/update-organization-member.md) | `PUT /organization_members/:code` | [docs](https://developer.whattime.co.kr/swagger#/Organization/organizationMemberUpdate) |
| [Update Routing Form](actions/update-routing-form.md) | `PUT /routing_forms/:code` | [docs](https://developer.whattime.co.kr/swagger#/RoutingForm/routingFormsUpdate) |
| [Update User](actions/update-user.md) | `PUT /users/:code` | [docs](https://developer.whattime.co.kr/swagger#/User/usersUpdate) |
| [Upsert Calendar](actions/upsert-calendar.md) | `POST /calendars/upsert` | [docs](https://developer.whattime.co.kr/swagger#/Calendar/calendarsUpsert) |
