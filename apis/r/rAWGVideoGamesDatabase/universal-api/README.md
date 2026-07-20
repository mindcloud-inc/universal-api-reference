# <img src="https://images.mindcloud.co/apps/icons/favicon-rawg-io-48x48_1775760965954.png" alt="RAWG Video Games Database logo" width="28" height="28"> RAWG Video Games Database: Universal API

Browse RAWG video game data, including games, platforms, stores, genres, tags, creators, developers, publishers, screenshots, trailers, achievements, and related media.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rAWGVideoGamesDatabase/latest
- **Category:** IT Operations / Database
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://rawg.io/
- **Vendor API docs:** https://rawg.io/apidocs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Games](actions/list-games.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rAWGVideoGamesDatabase/latest/actions/list-games?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [List Games](actions/list-games.md) | GET | Retrieves games from RAWG Video Games Database. |

