# <img src="https://images.mindcloud.co/apps/icons/precisely_1774373969374.png" alt="Precisely logo" width="28" height="28"> Precisely: Universal API

Geocode addresses, resolve PreciselyIDs, enrich locations, and retrieve geographic datasets like time zones, schools, speed limits, and intersections.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/precisely/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.precisely.com/precisely-apis/
- **Vendor API docs:** https://docs.precisely.com/docs/sftw/precisely-apis/main/en-us/webhelp/apis/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Typeahead Locations](actions/typeahead-locations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/precisely/latest/actions/typeahead-locations?connectionId=$CONNECTION_ID&searchText=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Intersection

| Action | Method | Description |
| --- | --- | --- |
| [Nearest Intersection By Location](actions/nearest-intersection-by-location.md) | GET | Retrieves the nearest intersection from Precisely by location. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Geocode Address (Basic)](actions/geocode-address-basic.md) | GET | Retrieves geocoding candidates from Precisely for an address. |
| [Key Lookup](actions/key-lookup.md) | GET | Retrieves an address from Precisely by PreciselyID or EIR code. |
| [Location By IP Address](actions/location-by-ip-address.md) | GET | Retrieves location coordinates from Precisely by IP address. |
| [Reverse Geocode (Basic)](actions/reverse-geocode-basic.md) | GET | Retrieves address details from Precisely for a coordinate. |
| [Typeahead Locations](actions/typeahead-locations.md) | GET | Finds address suggestions in Precisely by partial location input. |

### Preciselyid

| Action | Method | Description |
| --- | --- | --- |
| [Get PreciselyID By Address](actions/get-preciselyid-by-address.md) | GET | Retrieves a PreciselyID for an address in Precisely. |

### Roadsegment

| Action | Method | Description |
| --- | --- | --- |
| [Nearest Speed Limit](actions/nearest-speed-limit.md) | GET | Retrieves the nearest speed limit from Precisely by location. |

### School

| Action | Method | Description |
| --- | --- | --- |
| [Nearby Schools By Address](actions/nearby-schools-by-address.md) | GET | Retrieves nearby schools from Precisely by address. |

### Timezone

| Action | Method | Description |
| --- | --- | --- |
| [Timezone By Address](actions/timezone-by-address.md) | GET | Retrieves time zone details from Precisely by address. |
| [Timezone By Location](actions/timezone-by-location.md) | GET | Retrieves time zone details from Precisely by location. |

