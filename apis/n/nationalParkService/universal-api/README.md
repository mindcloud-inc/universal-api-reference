# <img src="https://images.mindcloud.co/apps/icons/nps-icon_1777558702382.png" alt="National Park Service logo" width="28" height="28"> National Park Service: Universal API

Access authoritative National Park Service data and content about parks, alerts, campgrounds, visitor centers, events, articles, media, and trip-planning resources.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nationalParkService/latest
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.nps.gov/subjects/developer/
- **Vendor API docs:** https://www.nps.gov/subjects/developer/api-documentation.htm

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Parks](actions/list-parks.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nationalParkService/latest/actions/list-parks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [List Activities](actions/list-activities.md) | GET | Retrieves activities from National Park Service. |

### Alert

| Action | Method | Description |
| --- | --- | --- |
| [List Alerts](actions/list-alerts.md) | GET | Retrieves alerts from National Park Service. |

### Amenity

| Action | Method | Description |
| --- | --- | --- |
| [List Amenities](actions/list-amenities.md) | GET | Retrieves amenities from National Park Service. |

### Article

| Action | Method | Description |
| --- | --- | --- |
| [List Articles](actions/list-articles.md) | GET | Retrieves articles from National Park Service. |

### Audio

| Action | Method | Description |
| --- | --- | --- |
| [List Audio](actions/list-audio.md) | GET | Retrieves audio resources from National Park Service. |

### Campground

| Action | Method | Description |
| --- | --- | --- |
| [List Campgrounds](actions/list-campgrounds.md) | GET | Retrieves campgrounds from National Park Service. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [List Events](actions/list-events.md) | GET | Retrieves events from National Park Service. |

### Fee Or Pass

| Action | Method | Description |
| --- | --- | --- |
| [List Fees And Passes](actions/list-fees-and-passes.md) | GET | Retrieves fees and passes from National Park Service. |

### Gallery

| Action | Method | Description |
| --- | --- | --- |
| [List Galleries](actions/list-galleries.md) | GET | Retrieves galleries from National Park Service. |

### Gallery Asset

| Action | Method | Description |
| --- | --- | --- |
| [List Gallery Assets](actions/list-gallery-assets.md) | GET | Retrieves gallery assets from National Park Service. |

### Lesson Plan

| Action | Method | Description |
| --- | --- | --- |
| [List Lesson Plans](actions/list-lesson-plans.md) | GET | Retrieves lesson plans from National Park Service. |

### News Release

| Action | Method | Description |
| --- | --- | --- |
| [List News Releases](actions/list-news-releases.md) | GET | Retrieves news releases from National Park Service. |

### Park

| Action | Method | Description |
| --- | --- | --- |
| [List Parks](actions/list-parks.md) | GET | Retrieves parks from National Park Service. |

### Parking Lot

| Action | Method | Description |
| --- | --- | --- |
| [List Parking Lots](actions/list-parking-lots.md) | GET | Retrieves parking lots from National Park Service. |

### Passport Stamp Location

| Action | Method | Description |
| --- | --- | --- |
| [List Passport Stamp Locations](actions/list-passport-stamp-locations.md) | GET | Retrieves passport stamp locations from National Park Service. |

### Person Article

| Action | Method | Description |
| --- | --- | --- |
| [List People](actions/list-people.md) | GET | Retrieves people from National Park Service. |

### Place Article

| Action | Method | Description |
| --- | --- | --- |
| [List Places](actions/list-places.md) | GET | Retrieves places from National Park Service. |

### Road Event

| Action | Method | Description |
| --- | --- | --- |
| [List Road Events](actions/list-road-events.md) | GET | Retrieves road events from National Park Service. |

### Thing To Do

| Action | Method | Description |
| --- | --- | --- |
| [List Things To Do](actions/list-things-to-do.md) | GET | Retrieves things to do from National Park Service. |

### Topic

| Action | Method | Description |
| --- | --- | --- |
| [List Topics](actions/list-topics.md) | GET | Retrieves topics from National Park Service. |

### Tour

| Action | Method | Description |
| --- | --- | --- |
| [List Tours](actions/list-tours.md) | GET | Retrieves tours from National Park Service. |

### Video

| Action | Method | Description |
| --- | --- | --- |
| [List Videos](actions/list-videos.md) | GET | Retrieves videos from National Park Service. |

### Visitor Center

| Action | Method | Description |
| --- | --- | --- |
| [List Visitor Centers](actions/list-visitor-centers.md) | GET | Retrieves visitor centers from National Park Service. |

### Webcam

| Action | Method | Description |
| --- | --- | --- |
| [List Webcams](actions/list-webcams.md) | GET | Retrieves webcams from National Park Service. |

