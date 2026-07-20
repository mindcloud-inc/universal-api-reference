# <img src="https://images.mindcloud.co/apps/icons/images-13_1774634443561.jpeg" alt="Evenium logo" width="28" height="28"> Evenium: Universal API

Evenium is an event management and guest registration platform for organizers to manage events, guests, registrations, and related event operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/evenium/latest
- **Category:** Marketing / Events & Webinars
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://evenium.com
- **Vendor API docs:** https://static.evenium.com/api-docs/organizer/index-json.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Events](actions/list-events.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evenium/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Evenium. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Evenium. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Evenium. |
| [Get Contact by Custom ID](actions/get-contact-by-custom-id.md) | GET | Retrieves a contact from Evenium by custom ID. |
| [Import Contacts](actions/import-contacts.md) | PUT | Imports contacts into Evenium. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Evenium. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Evenium. |
| [Update Contact by Custom ID](actions/update-contact-by-custom-id.md) | PUT | Updates a contact in Evenium by custom ID. |

### Event Part Registrations

| Action | Method | Description |
| --- | --- | --- |
| [List Event Part Registrations](actions/list-event-part-registrations.md) | GET | Retrieves event part registrations from Evenium. |

### Event Parts

| Action | Method | Description |
| --- | --- | --- |
| [Get Event Part](actions/get-event-part.md) | GET | Retrieves an event part from Evenium. |
| [List Event Parts](actions/list-event-parts.md) | GET | Retrieves event parts from Evenium. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST | Creates a new event in Evenium. |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from Evenium. |
| [List Contact Events](actions/list-contact-events.md) | GET | Retrieves a contact's events from Evenium. |
| [List Contact Events by Custom ID](actions/list-contact-events-by-custom-id.md) | GET | Retrieves a contact's events from Evenium by custom ID. |
| [List Events](actions/list-events.md) | GET | Retrieves events from Evenium. |

### Guest Accommodations

| Action | Method | Description |
| --- | --- | --- |
| [List Guest Accommodations](actions/list-guest-accommodations.md) | GET | Retrieves guest accommodations from Evenium. |

### Guest Post Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Guest Post Status](actions/get-guest-post-status.md) | GET | Retrieves a guest post status from Evenium. |

### Guest Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Guest Status](actions/get-guest-status.md) | GET | Retrieves a guest status from Evenium. |

### Guests

| Action | Method | Description |
| --- | --- | --- |
| [Create Guest](actions/create-guest.md) | POST | Creates a new guest in Evenium. |
| [Get Guest](actions/get-guest.md) | GET | Retrieves a guest from Evenium. |
| [Import Guests](actions/import-guests.md) | PUT | Imports guests into Evenium. |
| [List Guests](actions/list-guests.md) | GET | Retrieves guests from Evenium. |
| [Update Guest](actions/update-guest.md) | PUT | Updates an existing guest in Evenium. |
| [Update Guest Photo](actions/update-guest-photo.md) | PUT | Updates a guest photo in Evenium. |
| [Update Guest Post Status](actions/update-guest-post-status.md) | PUT | Updates a guest post status in Evenium. |
| [Update Guest Status](actions/update-guest-status.md) | PUT | Updates a guest status in Evenium. |

### Hotels

| Action | Method | Description |
| --- | --- | --- |
| [List Hotels](actions/list-hotels.md) | GET | Retrieves hotels from Evenium. |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Log In](actions/log-in.md) | GET | Retrieves an access token from Evenium. |
| [Log Out](actions/log-out.md) | GET | Logs out of Evenium. |

