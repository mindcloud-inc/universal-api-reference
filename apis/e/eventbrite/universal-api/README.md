# <img src="https://images.mindcloud.co/apps/icons/eventbrite_1772654187273.png" alt="Eventbrite logo" width="28" height="28"> Eventbrite: Universal API

Create events, manage attendees, orders, venues, and organizers

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/eventbrite/latest
- **Category:** Support / Ticketing
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.eventbrite.com
- **Vendor API docs:** https://www.eventbrite.com/platform/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List My Organizations](actions/list-my-organizations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/list-my-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Addresses

| Action | Method | Description |
| --- | --- | --- |
| [Create Organization Venue](actions/create-organization-venue.md) | POST | Creates a new organization venue in Eventbrite. |
| [Get Venue](actions/get-venue.md) | GET | Retrieves a venue from Eventbrite. |
| [List Organization Venues](actions/list-organization-venues.md) | GET | Retrieves organization venues from Eventbrite. |
| [Update Venue](actions/update-venue.md) | PUT | Updates an existing venue in Eventbrite. |

### Attendees

| Action | Method | Description |
| --- | --- | --- |
| [Get Attendee](actions/get-attendee.md) | GET | Retrieves an attendee from Eventbrite. |
| [List Event Attendees](actions/list-event-attendees.md) | GET | Retrieves event attendees from Eventbrite. |
| [List Organization Attendees](actions/list-organization-attendees.md) | GET | Retrieves organization attendees from Eventbrite. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [List Organization Events](actions/list-organization-events.md) | GET | Retrieves organization events from Eventbrite. |
| [List Venue Events](actions/list-venue-events.md) | GET | Retrieves venue events from Eventbrite. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Copy Event](actions/copy-event.md) | POST | Copies an event in Eventbrite. |
| [Create Organization Event](actions/create-organization-event.md) | POST | Creates a new organization event in Eventbrite. |
| [Delete Event](actions/delete-event.md) | DELETE | Deletes an existing event from Eventbrite. |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from Eventbrite. |
| [List Organizer Events](actions/list-organizer-events.md) | GET | Retrieves organizer events from Eventbrite. |
| [Publish Event](actions/publish-event.md) | PUT | Publishes an event in Eventbrite. |
| [Unpublish Event](actions/unpublish-event.md) | PUT | Unpublishes an event in Eventbrite. |
| [Update Event](actions/update-event.md) | PUT | Updates an existing event in Eventbrite. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from Eventbrite. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [List Event Orders](actions/list-event-orders.md) | GET | Retrieves event orders from Eventbrite. |
| [List Organization Orders](actions/list-organization-orders.md) | GET | Retrieves organization orders from Eventbrite. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [List My Organizations](actions/list-my-organizations.md) | GET | Retrieves your organizations from Eventbrite. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Attendees Report](actions/get-organization-attendees-report.md) | GET | Retrieves an organization attendees report from Eventbrite. |
| [Get Organization Sales Report](actions/get-organization-sales-report.md) | GET | Retrieves an organization sales report from Eventbrite. |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [Create Event Ticket Class](actions/create-event-ticket-class.md) | POST | Creates a new event ticket class in Eventbrite. |
| [List Event Ticket Classes](actions/list-event-ticket-classes.md) | GET | Retrieves event ticket classes from Eventbrite. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Eventbrite. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create Organization Organizer](actions/create-organization-organizer.md) | POST | Creates a new organization organizer in Eventbrite. |
| [Get Organizer](actions/get-organizer.md) | GET | Retrieves an organizer from Eventbrite. |
| [List Organization Organizers](actions/list-organization-organizers.md) | GET | Retrieves organization organizers from Eventbrite. |
| [Update Organizer](actions/update-organizer.md) | PUT | Updates an existing organizer in Eventbrite. |

