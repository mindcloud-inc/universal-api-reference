# Ticketmaster: Native API Reference

A consolidated summary of Ticketmaster's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://developer.ticketmaster.com/products-and-docs/apis/discovery-api/v2/
- **API base URL:** `https://app.ticketmaster.com`

## Authentication

### API Key

Use your Ticketmaster consumer key as the API key for Discovery API v2.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.ticketmaster.com/products-and-docs/apis/discovery-api/v2/)

## API conventions

The total page count is read from `page.totalPages`. The current page number is read from `page.number`.

## Pagination

Use `size` in the query string to set the page size (default 20; accepted range 1–200). Use `page` in the query string to choose the page; numbering starts at 0.

## Sorting

Set the sort field with `sort` in the query string. Only one sort field is accepted.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Find Suggest](actions/find-suggest.md) | `GET /discovery/v2/suggest.json` | [docs](https://developer.ticketmaster.com/products-and-docs/apis/discovery-api/v2/#finding-events-v2) |
| [Get Attraction](actions/get-attraction.md) | `GET /discovery/v2/attractions/:id` | [docs](https://developer.ticketmaster.com/products-and-docs/apis/discovery-api/v2/#search-attractions-v2) |
| [Get Classification](actions/get-classification.md) | `GET /discovery/v2/classifications/:id` | [docs](https://developer.ticketmaster.com/products-and-docs/apis/discovery-api/v2/#search-classifications-v2) |
| [Get Event](actions/get-event.md) | `GET /discovery/v2/events/:id` | [docs](https://developer.ticketmaster.com/products-and-docs/apis/discovery-api/v2/#event-details-v2) |
| [Get Event Images](actions/get-event-images.md) | `GET /discovery/v2/events/:id/images` | [docs](https://developer.ticketmaster.com/products-and-docs/apis/discovery-api/v2/#event-images-v2) |
| [Get Genre](actions/get-genre.md) | `GET /discovery/v2/classifications/genres/:id` | [docs](https://developer.ticketmaster.com/products-and-docs/apis/discovery-api/v2/#search-genres-v2) |
| [Get Segment](actions/get-segment.md) | `GET /discovery/v2/classifications/segments/:id` | [docs](https://developer.ticketmaster.com/products-and-docs/apis/discovery-api/v2/#segment-details-v2) |
| [Get Sub-Genre](actions/get-sub-genre.md) | `GET /discovery/v2/classifications/subgenres/:id` | [docs](https://developer.ticketmaster.com/products-and-docs/apis/discovery-api/v2/#search-subgenres-v2) |
| [Get Venue](actions/get-venue.md) | `GET /discovery/v2/venues/:id` | [docs](https://developer.ticketmaster.com/products-and-docs/apis/discovery-api/v2/#search-venues-v2) |
| [List Attractions](actions/list-attractions.md) | `GET /discovery/v2/attractions` | [docs](https://developer.ticketmaster.com/products-and-docs/apis/discovery-api/v2/#search-attractions-v2) |
| [List Classifications](actions/list-classifications.md) | `GET /discovery/v2/classifications` | [docs](https://developer.ticketmaster.com/products-and-docs/apis/discovery-api/v2/#search-classifications-v2) |
| [List Events](actions/list-events.md) | `GET /discovery/v2/events` | [docs](https://developer.ticketmaster.com/products-and-docs/apis/discovery-api/v2/#overview) |
| [List Venues](actions/list-venues.md) | `GET /discovery/v2/venues` | [docs](https://developer.ticketmaster.com/products-and-docs/apis/discovery-api/v2/#search-venues-v2) |
