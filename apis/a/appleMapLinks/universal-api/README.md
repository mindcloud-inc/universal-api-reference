# <img src="https://images.mindcloud.co/apps/icons/apple-maps-logo-3d_1780948752612.png" alt="Apple Map Links logo" width="28" height="28"> Apple Map Links: Universal API

Generate documented Apple Maps links for map framing, search, place cards, Look Around, directions, guides, reports, and legacy map-link formats.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/appleMapLinks/latest
- **Category:** Support / Field Service
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://maps.apple.com
- **Vendor API docs:** https://developer.apple.com/documentation/mapkit/unified-map-urls

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Frame Map](actions/frame-map.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appleMapLinks/latest/actions/frame-map?connectionId=$CONNECTION_ID&center=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Frame Map](actions/frame-map.md) | GET | Frames a map view in Apple Maps. |
| [Get Directions](actions/get-directions.md) | GET | Opens Apple Maps directions between locations. |
| [Legacy Address Map Link](actions/legacy-address-map-link.md) | GET | Shows an Apple Maps address using the legacy map link. |
| [Legacy Coordinate Map Link](actions/legacy-coordinate-map-link.md) | GET | Shows an Apple Maps coordinate using the legacy map link. |
| [Legacy Directions Map Link](actions/legacy-directions-map-link.md) | GET | Opens Apple Maps directions using the legacy map link. |
| [Legacy Search Map Link](actions/legacy-search-map-link.md) | GET | Searches Apple Maps using the legacy map link. |
| [Open Guides](actions/open-guides.md) | GET | Opens guides and curated collections in Apple Maps. |
| [Open Look Around By Address](actions/open-look-around-by-address.md) | GET | Opens Apple Maps Look Around by address. |
| [Open Look Around By Coordinate](actions/open-look-around-by-coordinate.md) | GET | Opens Apple Maps Look Around by coordinate. |
| [Open Look Around By Place ID](actions/open-look-around-by-place-id.md) | GET | Opens Apple Maps Look Around by Place ID. |
| [Report Problem By Address](actions/report-problem-by-address.md) | GET | Opens Apple Maps problem reporting by address. |
| [Report Problem By Coordinate](actions/report-problem-by-coordinate.md) | GET | Opens Apple Maps problem reporting by coordinate. |
| [Report Problem By Place ID](actions/report-problem-by-place-id.md) | GET | Opens Apple Maps problem reporting by Place ID. |
| [Search Maps](actions/search-maps.md) | GET | Searches Apple Maps for places or addresses. |
| [Show Place By Address](actions/show-place-by-address.md) | GET | Shows an Apple Maps place card by address. |
| [Show Place By Coordinate](actions/show-place-by-coordinate.md) | GET | Shows an Apple Maps place card by coordinate. |
| [Show Place By Place ID](actions/show-place-by-place-id.md) | GET | Shows an Apple Maps place card by Place ID. |

