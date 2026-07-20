# <img src="https://images.mindcloud.co/apps/icons/open-elevation_1777559649679.png" alt="Open-Elevation logo" width="28" height="28"> Open-Elevation: Universal API

Look up terrain elevation for geographic coordinates

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/openElevation/latest
- **Category:** Support / Field Service
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.open-elevation.com
- **Vendor API docs:** https://github.com/Jorl17/open-elevation/blob/master/docs/api.md

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Look Up Elevation](actions/look-up-elevation.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openElevation/latest/actions/look-up-elevation?connectionId=$CONNECTION_ID&locations=41.161758%2C-8.583933" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Elevation Result

| Action | Method | Description |
| --- | --- | --- |
| [Look Up Elevation](actions/look-up-elevation.md) | GET | Retrieves elevations from Open-Elevation for coordinates in the query string. |
| [Look Up Elevations From Body](actions/look-up-elevations-from-body.md) | GET | Retrieves elevations from Open-Elevation for coordinates in the request body. |

