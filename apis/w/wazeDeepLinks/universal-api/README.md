# <img src="https://images.mindcloud.co/apps/icons/waze-deep-links_1775959422323.png" alt="Waze Deep Links logo" width="28" height="28"> Waze Deep Links: Universal API

Generate documented Waze deep link URLs for search, map display, favorites, and navigation.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/wazeDeepLinks/latest
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.waze.com
- **Vendor API docs:** https://developers.google.com/waze/deeplinks

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Address](actions/search-address.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wazeDeepLinks/latest/actions/search-address?connectionId=$CONNECTION_ID&q=66%20Acacia%20Avenue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Navigate To Coordinates](actions/navigate-to-coordinates.md) | GET | Generates a Waze navigation URL for map coordinates. |
| [Navigate To Favorite](actions/navigate-to-favorite.md) | GET | Generates a Waze navigation URL to a saved favorite. |
| [Search Address](actions/search-address.md) | GET | Generates a Waze deep link URL to search an address. |
| [Search And Navigate](actions/search-and-navigate.md) | GET | Generates a Waze navigation URL from a search query. |
| [Show Location On Map](actions/show-location-on-map.md) | GET | Generates a Waze map URL for coordinates and zoom. |
| [Show Map At Zoom Level](actions/show-map-at-zoom-level.md) | GET | Generates a Waze map URL for a zoom level. |

