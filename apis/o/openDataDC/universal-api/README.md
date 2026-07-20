# <img src="https://images.mindcloud.co/apps/icons/open-data-dc-icon_1776706568658.png" alt="Open Data DC logo" width="28" height="28"> Open Data DC: Universal API

Access DC Master Address Repository geocoding, reverse geocoding, autocomplete, SSL, unit, and zone lookup endpoints from the MAR 2 Open Data DC API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/openDataDC/latest
- **Actions:** 34
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://opendata.dc.gov/
- **Vendor API docs:** https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Location By Address](actions/get-location-by-address.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/get-location-by-address?connectionId=$CONNECTION_ID&address=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (34)

### Autocomplete

| Action | Method | Description |
| --- | --- | --- |
| [Autocomplete Address](actions/autocomplete-address.md) | GET |  |
| [Autocomplete Address From Body](actions/autocomplete-address-from-body.md) | GET |  |
| [Autocomplete Address With POST](actions/autocomplete-address-with-post.md) | GET |  |

### Batch Geocoding

| Action | Method | Description |
| --- | --- | --- |
| [Create Location Batch](actions/create-location-batch.md) | POST |  |
| [Create Location Batch With Path Options](actions/create-location-batch-with-path-options.md) | POST |  |
| [Get Location Batch](actions/get-location-batch.md) | GET |  |
| [Get Location Batch With Query Options](actions/get-location-batch-with-query-options.md) | GET |  |

### Geocoding

| Action | Method | Description |
| --- | --- | --- |
| [Create Location By Address And Zones From Body](actions/create-location-by-address-and-zones-from-body.md) | POST |  |
| [Create Location By Address From Body](actions/create-location-by-address-from-body.md) | POST |  |
| [Create Location By Address With Zones](actions/create-location-by-address-with-zones.md) | POST |  |
| [Get Location By Address](actions/get-location-by-address.md) | GET |  |
| [Get Location By Address With Zones](actions/get-location-by-address-with-zones.md) | GET |  |

### Reverse Geocoding

| Action | Method | Description |
| --- | --- | --- |
| [Create Locations By Coordinates](actions/create-locations-by-coordinates.md) | POST |  |
| [Create Locations By Coordinates From Body](actions/create-locations-by-coordinates-from-body.md) | POST |  |
| [Create Locations By Coordinates With Zones](actions/create-locations-by-coordinates-with-zones.md) | POST |  |
| [Create Nearest Locations By Coordinates](actions/create-nearest-locations-by-coordinates.md) | POST |  |
| [Create Nearest Locations By Coordinates With Count](actions/create-nearest-locations-by-coordinates-with-count.md) | POST |  |
| [Create Nearest Locations From Body](actions/create-nearest-locations-from-body.md) | POST |  |
| [Get Locations By Coordinates](actions/get-locations-by-coordinates.md) | GET |  |
| [Get Locations By Coordinates With Zones](actions/get-locations-by-coordinates-with-zones.md) | GET |  |
| [Get Nearest Locations By Coordinates](actions/get-nearest-locations-by-coordinates.md) | GET |  |
| [Get Nearest Locations By Coordinates With Count](actions/get-nearest-locations-by-coordinates-with-count.md) | GET |  |

### Ssl

| Action | Method | Description |
| --- | --- | --- |
| [Create SSL Lookup](actions/create-ssl-lookup.md) | POST |  |
| [Create SSL Lookup By Identifier](actions/create-ssl-lookup-by-identifier.md) | POST |  |
| [Get SSL By Identifier](actions/get-ssl-by-identifier.md) | GET |  |
| [Search SSLs](actions/search-ssls.md) | GET |  |

### Unit

| Action | Method | Description |
| --- | --- | --- |
| [Create Unit Lookup](actions/create-unit-lookup.md) | POST |  |
| [Create Units Lookup By MAR ID](actions/create-units-lookup-by-mar-id.md) | POST |  |
| [Create Units Lookup By MAR ID And Type](actions/create-units-lookup-by-mar-id-and-type.md) | POST |  |
| [Get Units By MAR ID](actions/get-units-by-mar-id.md) | GET |  |
| [Get Units By MAR ID And Type](actions/get-units-by-mar-id-and-type.md) | GET |  |
| [Search Units](actions/search-units.md) | GET |  |

### Zone

| Action | Method | Description |
| --- | --- | --- |
| [Create Zone Lookup](actions/create-zone-lookup.md) | POST |  |
| [Get Zone](actions/get-zone.md) | GET |  |

