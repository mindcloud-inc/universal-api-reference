# <img src="https://images.mindcloud.co/apps/icons/o-mdb_1777575636953.png" alt="OMDb logo" width="28" height="28"> OMDb: Universal API

Search movies, series, and episodes by title or IMDb ID

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/oMDb/latest
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.omdbapi.com
- **Vendor API docs:** https://www.omdbapi.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Title by IMDb ID](actions/get-title-by-imdb-id.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oMDb/latest/actions/get-title-by-imdb-id?connectionId=$CONNECTION_ID&imdbId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Episode

| Action | Method | Description |
| --- | --- | --- |
| [Get Episode by IMDb ID](actions/get-episode-by-imdb-id.md) | GET | Retrieves an episode from OMDb by series IMDb ID, season, and episode. |
| [Get Episode by Series Title](actions/get-episode-by-series-title.md) | GET | Retrieves an episode from OMDb by series title, season, and episode. |

### Movie

| Action | Method | Description |
| --- | --- | --- |
| [Get Movie by Title](actions/get-movie-by-title.md) | GET | Retrieves movie details from OMDb by title. |

### Season

| Action | Method | Description |
| --- | --- | --- |
| [Get Season by IMDb ID](actions/get-season-by-imdb-id.md) | GET | Retrieves a season from OMDb by series IMDb ID and season. |
| [Get Season by Series Title](actions/get-season-by-series-title.md) | GET | Retrieves a season from OMDb by series title and season. |

### Series

| Action | Method | Description |
| --- | --- | --- |
| [Get Series by Title](actions/get-series-by-title.md) | GET | Retrieves series details from OMDb by title. |

### Title

| Action | Method | Description |
| --- | --- | --- |
| [Get Title by IMDb ID](actions/get-title-by-imdb-id.md) | GET | Retrieves title details from OMDb by IMDb ID. |
| [Get Title by Title](actions/get-title-by-title.md) | GET | Retrieves title details from OMDb by title. |
| [Search Movies](actions/search-movies.md) | GET | Finds movies in OMDb by search term. |
| [Search Series](actions/search-series.md) | GET | Finds series in OMDb by search term. |
| [Search Titles](actions/search-titles.md) | GET | Finds titles in OMDb by search term. |

