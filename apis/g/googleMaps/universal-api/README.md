# <img src="https://images.mindcloud.co/apps/icons/google-maps-icon_1782393644234.png" alt="Google Maps logo" width="28" height="28"> Google Maps: Universal API

Google Maps through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/googleMaps/latest
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Geocode Address](actions/geocode-address.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleMaps/latest/actions/geocode-address?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Addresses

| Action | Method | Description |
| --- | --- | --- |
| [Validate Address](actions/validate-address.md) | POST | Validates an Address |

### Geocoding

| Action | Method | Description |
| --- | --- | --- |
| [Geocode Address](actions/geocode-address.md) | GET |  |

### Route Matrix

| Action | Method | Description |
| --- | --- | --- |
| [Get Route Matrix](actions/get-route-matrix.md) | GET |  |

