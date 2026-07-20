# National Park Service: Native API Reference

A consolidated summary of National Park Service's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://www.nps.gov/subjects/developer/api-documentation.htm
- **OpenAPI specification:** https://www.nps.gov/subjects/developer/customcf/swagger.json?03142019
- **API base URL:** `https://developer.nps.gov/api/v1`

## Authentication

### NPS API Key

API key authentication for the National Park Service API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://www.nps.gov/subjects/developer/guides.htm)

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–50). Use `start` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Activities](actions/list-activities.md) | `GET /activities` | [docs](https://www.nps.gov/subjects/developer/api-documentation.htm) |
| [List Alerts](actions/list-alerts.md) | `GET /alerts` | [docs](https://www.nps.gov/subjects/developer/api-documentation.htm) |
| [List Amenities](actions/list-amenities.md) | `GET /amenities` | [docs](https://www.nps.gov/subjects/developer/api-documentation.htm) |
| [List Articles](actions/list-articles.md) | `GET /articles` | [docs](https://www.nps.gov/subjects/developer/api-documentation.htm) |
| [List Audio](actions/list-audio.md) | `GET /multimedia/audio` | [docs](https://www.nps.gov/subjects/developer/api-documentation.htm) |
| [List Campgrounds](actions/list-campgrounds.md) | `GET /campgrounds` | [docs](https://www.nps.gov/subjects/developer/api-documentation.htm) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://www.nps.gov/subjects/developer/api-documentation.htm) |
| [List Fees And Passes](actions/list-fees-and-passes.md) | `GET /feespasses` | [docs](https://www.nps.gov/subjects/developer/api-documentation.htm) |
| [List Galleries](actions/list-galleries.md) | `GET /multimedia/galleries` | [docs](https://www.nps.gov/subjects/developer/api-documentation.htm) |
| [List Gallery Assets](actions/list-gallery-assets.md) | `GET /multimedia/galleries/assets` | [docs](https://www.nps.gov/subjects/developer/api-documentation.htm) |
| [List Lesson Plans](actions/list-lesson-plans.md) | `GET /lessonplans` | [docs](https://www.nps.gov/subjects/developer/api-documentation.htm) |
| [List News Releases](actions/list-news-releases.md) | `GET /newsreleases` | [docs](https://www.nps.gov/subjects/developer/api-documentation.htm) |
| [List Parking Lots](actions/list-parking-lots.md) | `GET /parkinglots` | [docs](https://www.nps.gov/subjects/developer/api-documentation.htm) |
| [List Parks](actions/list-parks.md) | `GET /parks` | [docs](https://www.nps.gov/subjects/developer/api-documentation.htm) |
| [List Passport Stamp Locations](actions/list-passport-stamp-locations.md) | `GET /passportstamplocations` | [docs](https://www.nps.gov/subjects/developer/api-documentation.htm) |
| [List People](actions/list-people.md) | `GET /people` | [docs](https://www.nps.gov/subjects/developer/api-documentation.htm) |
| [List Places](actions/list-places.md) | `GET /places` | [docs](https://www.nps.gov/subjects/developer/api-documentation.htm) |
| [List Road Events](actions/list-road-events.md) | `GET /roadevents` | [docs](https://www.nps.gov/subjects/developer/api-documentation.htm) |
| [List Things To Do](actions/list-things-to-do.md) | `GET /thingstodo` | [docs](https://www.nps.gov/subjects/developer/api-documentation.htm) |
| [List Topics](actions/list-topics.md) | `GET /topics` | [docs](https://www.nps.gov/subjects/developer/api-documentation.htm) |
| [List Tours](actions/list-tours.md) | `GET /tours` | [docs](https://www.nps.gov/subjects/developer/api-documentation.htm) |
| [List Videos](actions/list-videos.md) | `GET /multimedia/videos` | [docs](https://www.nps.gov/subjects/developer/api-documentation.htm) |
| [List Visitor Centers](actions/list-visitor-centers.md) | `GET /visitorcenters` | [docs](https://www.nps.gov/subjects/developer/api-documentation.htm) |
| [List Webcams](actions/list-webcams.md) | `GET /webcams` | [docs](https://www.nps.gov/subjects/developer/api-documentation.htm) |
