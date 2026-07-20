# <img src="https://images.mindcloud.co/apps/icons/1200x630wa_1775501121722.png" alt="Mighty Tix logo" width="28" height="28"> Mighty Tix: Universal API

Admin GraphQL wrapper for managing accounts, events, sessions, ticket types, venues, users, and orders in Mighty Tix.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mightyTix/latest
- **Category:** Support / Ticketing
- **Actions:** 41
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mightytix.com
- **Vendor API docs:** https://mightytix.com/docs/admin-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mightyTix/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (41)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves account details from Mighty Tix. |
| [Update Account](actions/update-account.md) | PUT | Updates account details in Mighty Tix. |

### Admin Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Get Admin Access Token](actions/get-admin-access-token.md) | GET | Retrieves an admin access token from Mighty Tix. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST | Creates a new event in Mighty Tix. |
| [Delete Event](actions/delete-event.md) | DELETE | Deletes an existing event from Mighty Tix. |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from Mighty Tix. |
| [List Events](actions/list-events.md) | GET | Retrieves events from Mighty Tix. |
| [Update Event](actions/update-event.md) | PUT | Updates an existing event in Mighty Tix. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from Mighty Tix. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from Mighty Tix. |
| [Resend Order](actions/resend-order.md) | PUT | Resends an order in Mighty Tix. |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Add Session Ticket Types To Session](actions/add-session-ticket-types-to-session.md) | PUT | Adds session ticket types to a session in Mighty Tix. |
| [Create Or Update Session Ticket Types](actions/create-or-update-session-ticket-types.md) | PUT | Creates or updates session ticket types in Mighty Tix. |
| [Create Session](actions/create-session.md) | POST | Creates a new session in Mighty Tix. |
| [Delete Session](actions/delete-session.md) | DELETE | Deletes an existing session from Mighty Tix. |
| [Get Session](actions/get-session.md) | GET | Retrieves a session from Mighty Tix. |
| [List Sessions](actions/list-sessions.md) | GET | Retrieves sessions from Mighty Tix. |
| [Remove Session Ticket Types From Session](actions/remove-session-ticket-types-from-session.md) | PUT | Removes session ticket types from a session in Mighty Tix. |
| [Set Session Ticket Types On Session](actions/set-session-ticket-types-on-session.md) | PUT | Sets session ticket types on a session in Mighty Tix. |
| [Update Session](actions/update-session.md) | PUT | Updates an existing session in Mighty Tix. |

### Session Ticket Type

| Action | Method | Description |
| --- | --- | --- |
| [Create Session Ticket Type](actions/create-session-ticket-type.md) | POST | Creates a new session ticket type in Mighty Tix. |
| [Delete Session Ticket Type](actions/delete-session-ticket-type.md) | DELETE | Deletes an existing session ticket type from Mighty Tix. |
| [Get Session Ticket Type](actions/get-session-ticket-type.md) | GET | Retrieves a session ticket type from Mighty Tix. |
| [List Session Ticket Types](actions/list-session-ticket-types.md) | GET | Retrieves session ticket types from Mighty Tix. |
| [Update Session Ticket Type](actions/update-session-ticket-type.md) | PUT | Updates an existing session ticket type in Mighty Tix. |

### Ticket Type

| Action | Method | Description |
| --- | --- | --- |
| [Create Ticket Type](actions/create-ticket-type.md) | POST | Creates a new ticket type in Mighty Tix. |
| [Delete Ticket Type](actions/delete-ticket-type.md) | DELETE | Deletes an existing ticket type from Mighty Tix. |
| [Get Ticket Type](actions/get-ticket-type.md) | GET | Retrieves a ticket type from Mighty Tix. |
| [List Ticket Types](actions/list-ticket-types.md) | GET | Retrieves ticket types from Mighty Tix. |
| [Reorder Ticket Types](actions/reorder-ticket-types.md) | PUT | Reorders ticket types in Mighty Tix. |
| [Update Ticket Type](actions/update-ticket-type.md) | PUT | Updates an existing ticket type in Mighty Tix. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in Mighty Tix. |
| [Delete User](actions/delete-user.md) | DELETE | Deletes an existing user from Mighty Tix. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Mighty Tix. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Mighty Tix. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in Mighty Tix. |

### Venue

| Action | Method | Description |
| --- | --- | --- |
| [Create Venue](actions/create-venue.md) | POST | Creates a new venue in Mighty Tix. |
| [Delete Venue](actions/delete-venue.md) | DELETE | Deletes an existing venue from Mighty Tix. |
| [Get Venue](actions/get-venue.md) | GET | Retrieves a venue from Mighty Tix. |
| [List Venues](actions/list-venues.md) | GET | Retrieves venues from Mighty Tix. |
| [Update Venue](actions/update-venue.md) | PUT | Updates an existing venue in Mighty Tix. |

