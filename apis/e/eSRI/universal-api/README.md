# <img src="https://images.mindcloud.co/apps/icons/favicon-developers-arcgis-com-48x48_1776285979169.png" alt="ESRI logo" width="28" height="28"> ESRI: Universal API

ESRI wraps ArcGIS location services for geocoding, places, routing, and portal metadata workflows with an ArcGIS API key.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/eSRI/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.esri.com/
- **Vendor API docs:** https://developers.arcgis.com/rest/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Portal Self](actions/portal-self.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eSRI/latest/actions/portal-self?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Portal Self](actions/portal-self.md) | GET | Retrieves the current ArcGIS portal view. |

