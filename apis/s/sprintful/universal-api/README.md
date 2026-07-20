# <img src="https://images.mindcloud.co/apps/icons/images-18_1774636102939.png" alt="Sprintful logo" width="28" height="28"> Sprintful: Universal API

Manage booking pages, availability, and bookings in Sprintful

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sprintful/latest
- **Category:** Productivity / Scheduling
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sprintful.com
- **Vendor API docs:** https://support.sprintful.com/category/96-apis

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sprintful/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Availability

| Action | Method | Description |
| --- | --- | --- |
| [Get Availability](actions/get-availability.md) | GET | Retrieves booking page availability from Sprintful. |

### Booking

| Action | Method | Description |
| --- | --- | --- |
| [Get Booking](actions/get-booking.md) | GET | Retrieves a booking event from Sprintful. |
| [List Bookings](actions/list-bookings.md) | GET | Retrieves booking events available in Sprintful. |

### Booking Page

| Action | Method | Description |
| --- | --- | --- |
| [List Pages](actions/list-pages.md) | GET | Retrieves booking pages available in Sprintful. |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Get Page](actions/get-page.md) | GET | Retrieves a booking page from Sprintful. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Sprintful. |

