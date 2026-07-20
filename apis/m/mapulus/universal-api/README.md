# <img src="https://images.mindcloud.co/apps/icons/mapulus_1775490926716.png" alt="Mapulus logo" width="28" height="28"> Mapulus: Universal API

Explore, enrich, and query Australian location intelligence data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mapulus/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.mapulus.com
- **Vendor API docs:** https://developer.mapulus.com/v1/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Maps](actions/list-maps.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mapulus/latest/actions/list-maps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Create Location](actions/create-location.md) | POST | Creates a new location in Mapulus. |
| [Delete Location](actions/delete-location.md) | DELETE | Deletes an existing location from Mapulus. |
| [Get Location](actions/get-location.md) | GET | Retrieves a specific location from Mapulus. |
| [List Locations](actions/list-locations.md) | GET | Retrieves locations from your Mapulus account. |
| [Update Location](actions/update-location.md) | PUT | Updates an existing location in Mapulus. |

### Map

| Action | Method | Description |
| --- | --- | --- |
| [Get Map](actions/get-map.md) | GET | Retrieves a specific map from Mapulus. |
| [List Maps](actions/list-maps.md) | GET | Retrieves all maps from your Mapulus account. |

