# Mighty Tix: Native API Reference

A consolidated summary of Mighty Tix's API configuration and 41 documented operations, with links to official documentation.

- **Official docs:** https://mightytix.com/docs/admin-api
- **API base URL:** `https://mindcloudmttix260403.mightytix.com`

## Authentication

### Admin Login

Sign in to Mighty Tix Admin API with email and password to obtain a short-lived JWT bearer token.

### Credentials

- **Email:** `email` · required · Your Mighty Tix admin login email address.

Send these headers with each API request:

```http
Authorization: Bearer <custom.accessToken>
```

[Official authentication documentation](https://mightytix.com/docs/admin-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (41 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Session Ticket Types To Session](actions/add-session-ticket-types-to-session.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#mutation-addSessionTicketTypesToSession) |
| [Create Event](actions/create-event.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#mutation-createOneEvent) |
| [Create Or Update Session Ticket Types](actions/create-or-update-session-ticket-types.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#mutation-createOrUpdateSessionTicketTypes) |
| [Create Session](actions/create-session.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#mutation-createOneSession) |
| [Create Session Ticket Type](actions/create-session-ticket-type.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#mutation-createOneSessionTicketType) |
| [Create Ticket Type](actions/create-ticket-type.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#mutation-createOneTicketType) |
| [Create User](actions/create-user.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#mutation-createOneUser) |
| [Create Venue](actions/create-venue.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#mutation-createOneVenue) |
| [Delete Event](actions/delete-event.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#mutation-deleteOneEvent) |
| [Delete Session](actions/delete-session.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#mutation-deleteOneSession) |
| [Delete Session Ticket Type](actions/delete-session-ticket-type.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#mutation-deleteOneSessionTicketType) |
| [Delete Ticket Type](actions/delete-ticket-type.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#mutation-deleteOneTicketType) |
| [Delete User](actions/delete-user.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#mutation-deleteOneUser) |
| [Delete Venue](actions/delete-venue.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#mutation-deleteOneVenue) |
| [Get Account](actions/get-account.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#query-account) |
| [Get Admin Access Token](actions/get-admin-access-token.md) | `POST admin-api/auth/login` | [docs](https://mightytix.com/docs/admin-api#introduction-item-0) |
| [Get Event](actions/get-event.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#query-event) |
| [Get Order](actions/get-order.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#query-order) |
| [Get Session](actions/get-session.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#query-session) |
| [Get Session Ticket Type](actions/get-session-ticket-type.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#query-sessionTicketType) |
| [Get Ticket Type](actions/get-ticket-type.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#query-ticketType) |
| [Get User](actions/get-user.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#query-user) |
| [Get Venue](actions/get-venue.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#query-venue) |
| [List Events](actions/list-events.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#query-events) |
| [List Orders](actions/list-orders.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#query-orders) |
| [List Session Ticket Types](actions/list-session-ticket-types.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#query-sessionTicketTypes) |
| [List Sessions](actions/list-sessions.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#query-sessions) |
| [List Ticket Types](actions/list-ticket-types.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#query-ticketTypes) |
| [List Users](actions/list-users.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#query-users) |
| [List Venues](actions/list-venues.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#query-venues) |
| [Remove Session Ticket Types From Session](actions/remove-session-ticket-types-from-session.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#mutation-removeSessionTicketTypesFromSession) |
| [Reorder Ticket Types](actions/reorder-ticket-types.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#mutation-reorderTicketTypes) |
| [Resend Order](actions/resend-order.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#mutation-resendOrder) |
| [Set Session Ticket Types On Session](actions/set-session-ticket-types-on-session.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#mutation-setSessionTicketTypesOnSession) |
| [Update Account](actions/update-account.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#mutation-updateAccount) |
| [Update Event](actions/update-event.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#mutation-updateOneEvent) |
| [Update Session](actions/update-session.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#mutation-updateOneSession) |
| [Update Session Ticket Type](actions/update-session-ticket-type.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#mutation-updateOneSessionTicketType) |
| [Update Ticket Type](actions/update-ticket-type.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#mutation-updateOneTicketType) |
| [Update User](actions/update-user.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#mutation-updateOneUser) |
| [Update Venue](actions/update-venue.md) | `POST admin-api/graphql` | [docs](https://mightytix.com/docs/admin-api#mutation-updateOneVenue) |
