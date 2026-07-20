# <img src="https://images.mindcloud.co/apps/icons/veterans-affairs-facilities_1778005541120.png" alt="Veterans Affairs Facilities logo" width="28" height="28"> Veterans Affairs Facilities: Universal API

Find Department of Veterans Affairs facilities, facility IDs, contact details, addresses, available services, and drive-time nearby health facilities from the VA Facilities API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/veteransAffairsFacilities/latest
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.va.gov/find-locations/
- **Vendor API docs:** https://developer.va.gov/explore/api/va-facilities/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Facility IDs](actions/list-facility-ids.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veteransAffairsFacilities/latest/actions/list-facility-ids?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Nearby Va Facility

| Action | Method | Description |
| --- | --- | --- |
| [Find Nearby Facilities by Coordinates](actions/find-nearby-facilities-by-coordinates.md) | GET | Finds nearby VA facilities by coordinates and drive time. |

### Va Facility

| Action | Method | Description |
| --- | --- | --- |
| [Get Facilities by IDs](actions/get-facilities-by-ids.md) | GET | Retrieves VA facilities by facility IDs. |
| [Get Facility](actions/get-facility.md) | GET | Retrieves a VA facility by ID. |
| [Search Facilities by Bounding Box](actions/search-facilities-by-bounding-box.md) | GET | Finds VA facilities in a bounding box. |
| [Search Facilities by Coordinates](actions/search-facilities-by-coordinates.md) | GET | Finds VA facilities near latitude and longitude coordinates. |
| [Search Facilities by State](actions/search-facilities-by-state.md) | GET | Finds VA facilities in a state. |
| [Search Facilities by ZIP Code](actions/search-facilities-by-zip-code.md) | GET | Finds VA facilities near a ZIP code. |

### Va Facility Id

| Action | Method | Description |
| --- | --- | --- |
| [List Facility IDs](actions/list-facility-ids.md) | GET | Retrieves VA facility IDs by facility type. |

