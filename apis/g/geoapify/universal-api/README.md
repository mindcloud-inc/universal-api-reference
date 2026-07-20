# <img src="https://images.mindcloud.co/apps/icons/geoapify_1771628376584.png" alt="Geoapify Geocode logo" width="28" height="28"> Geoapify Geocode: Universal API

Search addresses, geocode locations, validate entries, and plan routes.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/geoapify/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.geoapify.com/
- **Vendor API docs:** https://apidocs.geoapify.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Forward Geocoding](actions/forward-geocoding.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geoapify/latest/actions/forward-geocoding?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Address Autocomplete](actions/address-autocomplete.md) | GET | Finds address and place suggestions in Geoapify. |
| [Forward Geocoding](actions/forward-geocoding.md) | GET | Finds locations in Geoapify by address. |
| [IP Geolocation](actions/ip-geolocation.md) | GET | Retrieves IP geolocation data from Geoapify. |
| [Postcode List](actions/postcode-list.md) | GET | Retrieves a filtered list of postcodes from Geoapify. |
| [Postcode Search](actions/postcode-search.md) | GET | Finds postcodes in Geoapify by location or value. |
| [Reverse Geocoding](actions/reverse-geocoding.md) | GET | Finds addresses in Geoapify by coordinates. |

