# <img src="https://images.mindcloud.co/apps/icons/opencage-icon-512_1776182633979.png" alt="OpenCage logo" width="28" height="28"> OpenCage: Universal API

OpenCage Geocoding API for forward and reverse geocoding using worldwide open data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/openCage/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://opencagedata.com
- **Vendor API docs:** https://opencagedata.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Forward Geocode](actions/forward-geocode.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openCage/latest/actions/forward-geocode?connectionId=$CONNECTION_ID&q=Frauenplan%201%2C%2099423%20Weimar%2C%20Germany" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Forward Geocode](actions/forward-geocode.md) | GET | Finds location details in OpenCage by address or place name. |
| [Reverse Geocode](actions/reverse-geocode.md) | GET | Retrieves location details from OpenCage by coordinates. |

