# <img src="https://images.mindcloud.co/apps/icons/79770758-2725-480d-b6f2-e887886c4332-2_1777581996224.png" alt="EONET logo" width="28" height="28"> EONET: Universal API

Track near real-time natural events and related imagery metadata from NASA's EONET API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/eONET/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://eonet.gsfc.nasa.gov
- **Vendor API docs:** https://eonet.gsfc.nasa.gov/docs/v3

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Events](actions/list-events.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eONET/latest/actions/list-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Atom Event Feed Item

| Action | Method | Description |
| --- | --- | --- |
| [List Atom Event Feed Items](actions/list-atom-event-feed-items.md) | GET | Retrieves Atom event feed items from EONET. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [List Categories](actions/list-categories.md) | GET | Retrieves categories from EONET. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from EONET. |
| [List Events](actions/list-events.md) | GET | Retrieves events from EONET. |
| [List Events for Category](actions/list-events-for-category.md) | GET | Retrieves events for a category from EONET. |

### Geojson Event Feature

| Action | Method | Description |
| --- | --- | --- |
| [List GeoJSON Event Features](actions/list-geojson-event-features.md) | GET | Retrieves GeoJSON event features from EONET. |
| [List GeoJSON Event Features for Event](actions/list-geojson-event-features-for-event.md) | GET | Retrieves GeoJSON event features for an event from EONET. |

### Layer Category

| Action | Method | Description |
| --- | --- | --- |
| [List Layers](actions/list-layers.md) | GET | Retrieves layers from EONET. |
| [List Layers for Category](actions/list-layers-for-category.md) | GET | Retrieves layers for a category from EONET. |

### Magnitude

| Action | Method | Description |
| --- | --- | --- |
| [List Magnitudes](actions/list-magnitudes.md) | GET | Retrieves magnitudes from EONET. |

### Rss Event Feed Item

| Action | Method | Description |
| --- | --- | --- |
| [List RSS Event Feed Items](actions/list-rss-event-feed-items.md) | GET | Retrieves RSS event feed items from EONET. |

### Source

| Action | Method | Description |
| --- | --- | --- |
| [List Sources](actions/list-sources.md) | GET | Retrieves sources from EONET. |

