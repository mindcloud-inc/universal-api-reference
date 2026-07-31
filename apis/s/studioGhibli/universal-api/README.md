# <img src="https://images.mindcloud.co/apps/icons/api-roulette-fallback-icon_1785423690162.png" alt="Studio Ghibli logo" width="28" height="28"> Studio Ghibli: Universal API

Studio Ghibli through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/studioGhibli/latest
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Film by ID](actions/get-film-by-id.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/studioGhibli/latest/actions/get-film-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Film

| Action | Method | Description |
| --- | --- | --- |
| [Get Film by ID](actions/get-film-by-id.md) | GET |  |
| [List Films](actions/list-films.md) | GET |  |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Get Location by ID](actions/get-location-by-id.md) | GET |  |
| [List Locations](actions/list-locations.md) | GET |  |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Get Person by ID](actions/get-person-by-id.md) | GET |  |
| [List People](actions/list-people.md) | GET |  |

### Species

| Action | Method | Description |
| --- | --- | --- |
| [Get Species by ID](actions/get-species-by-id.md) | GET |  |
| [List Species](actions/list-species.md) | GET |  |

### Vehicle

| Action | Method | Description |
| --- | --- | --- |
| [Get Vehicle by ID](actions/get-vehicle-by-id.md) | GET |  |
| [List Vehicles](actions/list-vehicles.md) | GET |  |

