# <img src="https://images.mindcloud.co/apps/icons/s-wapi_1785363209002.png" alt="SWAPI logo" width="28" height="28"> SWAPI: Universal API

Retrieve Star Wars reference data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sWAPI/latest
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://swapi.dev/
- **Vendor API docs:** https://swapi.dev/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Film](actions/get-film.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sWAPI/latest/actions/get-film?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Films

| Action | Method | Description |
| --- | --- | --- |
| [Get Film](actions/get-film.md) | GET |  |
| [List Films](actions/list-films.md) | GET |  |

### People

| Action | Method | Description |
| --- | --- | --- |
| [Get Person](actions/get-person.md) | GET |  |
| [List People](actions/list-people.md) | GET |  |

### Planets

| Action | Method | Description |
| --- | --- | --- |
| [Get Planet](actions/get-planet.md) | GET |  |
| [List Planets](actions/list-planets.md) | GET |  |

### Species

| Action | Method | Description |
| --- | --- | --- |
| [Get Species](actions/get-species.md) | GET |  |
| [List Species](actions/list-species.md) | GET |  |

### Starships

| Action | Method | Description |
| --- | --- | --- |
| [Get Starship](actions/get-starship.md) | GET |  |
| [List Starships](actions/list-starships.md) | GET |  |

### Vehicles

| Action | Method | Description |
| --- | --- | --- |
| [Get Vehicle](actions/get-vehicle.md) | GET |  |
| [List Vehicles](actions/list-vehicles.md) | GET |  |

