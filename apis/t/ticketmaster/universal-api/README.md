# <img src="https://images.mindcloud.co/apps/icons/ticketmaster-icon_1776692144421.png" alt="Ticketmaster logo" width="28" height="28"> Ticketmaster: Universal API

Search Ticketmaster Discovery API v2 for events, attractions, venues, classifications, and suggestions.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ticketmaster/latest
- **Category:** Support / Ticketing
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://developer.ticketmaster.com/
- **Vendor API docs:** https://developer.ticketmaster.com/products-and-docs/apis/discovery-api/v2/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Events](actions/list-events.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketmaster/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Attraction

| Action | Method | Description |
| --- | --- | --- |
| [Get Attraction](actions/get-attraction.md) | GET | Retrieves details for a specific attraction from Ticketmaster. |
| [List Attractions](actions/list-attractions.md) | GET | Finds attractions in Ticketmaster by name and related filters. |

### Classification

| Action | Method | Description |
| --- | --- | --- |
| [Get Classification](actions/get-classification.md) | GET | Retrieves details for a specific classification from Ticketmaster. |
| [List Classifications](actions/list-classifications.md) | GET | Finds classifications in Ticketmaster by name and related filters. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Event Images](actions/get-event-images.md) | GET | Retrieves images for a specific event from Ticketmaster. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Get Event](actions/get-event.md) | GET | Retrieves details for a specific event from Ticketmaster. |
| [List Events](actions/list-events.md) | GET | Finds events in Ticketmaster by location, date, and availability. |

### Genre

| Action | Method | Description |
| --- | --- | --- |
| [Get Genre](actions/get-genre.md) | GET | Retrieves details for a specific genre from Ticketmaster. |

### Segments

| Action | Method | Description |
| --- | --- | --- |
| [Get Segment](actions/get-segment.md) | GET | Retrieves details for a specific segment from Ticketmaster. |

### Sub Genre

| Action | Method | Description |
| --- | --- | --- |
| [Get Sub-Genre](actions/get-sub-genre.md) | GET | Retrieves details for a specific sub-genre from Ticketmaster. |

### Suggest

| Action | Method | Description |
| --- | --- | --- |
| [Find Suggest](actions/find-suggest.md) | GET | Finds search suggestions in Ticketmaster by keyword and filters. |

### Venue

| Action | Method | Description |
| --- | --- | --- |
| [Get Venue](actions/get-venue.md) | GET | Retrieves details for a specific venue from Ticketmaster. |
| [List Venues](actions/list-venues.md) | GET | Finds venues in Ticketmaster by name and related filters. |

