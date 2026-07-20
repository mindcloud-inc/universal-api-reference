# <img src="https://images.mindcloud.co/apps/icons/tvmaze-schedule-icon_1776796124529.png" alt="TVMaze Schedule logo" width="28" height="28"> TVMaze Schedule: Universal API

Access TVmaze's public TV schedule, show, episode, person, and update data through the free JSON REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tVMazeSchedule/latest
- **Actions:** 56
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.tvmaze.com
- **Vendor API docs:** https://www.tvmaze.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Alternate List](actions/get-alternate-list.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tVMazeSchedule/latest/actions/get-alternate-list?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (56)

### Alternate Episode

| Action | Method | Description |
| --- | --- | --- |
| [List Alternate Episodes](actions/list-alternate-episodes.md) | GET | Retrieves alternate episodes for a TVMaze list. |
| [List Alternate Episodes With Episodes](actions/list-alternate-episodes-with-episodes.md) | GET | Retrieves alternate episodes with episode details from TVMaze. |

### Alternate List

| Action | Method | Description |
| --- | --- | --- |
| [Get Alternate List](actions/get-alternate-list.md) | GET | Retrieves an alternate list from TVMaze. |
| [Get Alternate List With Alternate Episodes](actions/get-alternate-list-with-alternate-episodes.md) | GET | Retrieves a TVMaze alternate list with episodes. |
| [List Show Alternate Lists](actions/list-show-alternate-lists.md) | GET | Retrieves alternate lists for a TVMaze show. |

### Cast Credit

| Action | Method | Description |
| --- | --- | --- |
| [List Episode Guest Cast](actions/list-episode-guest-cast.md) | GET | Retrieves guest cast for a TVMaze episode. |
| [List Person Cast Credits](actions/list-person-cast-credits.md) | GET | Retrieves cast credits for a TVMaze person. |
| [List Person Cast Credits With Character](actions/list-person-cast-credits-with-character.md) | GET | Retrieves TVMaze cast credits with embedded characters. |
| [List Person Cast Credits With Show](actions/list-person-cast-credits-with-show.md) | GET | Retrieves TVMaze cast credits with embedded shows. |
| [List Person Guest Cast Credits](actions/list-person-guest-cast-credits.md) | GET | Retrieves guest cast credits for a TVMaze person. |
| [List Show Cast](actions/list-show-cast.md) | GET | Retrieves cast members for a TVMaze show. |

### Crew Credit

| Action | Method | Description |
| --- | --- | --- |
| [List Episode Guest Crew](actions/list-episode-guest-crew.md) | GET | Retrieves guest crew for a TVMaze episode. |
| [List Person Crew Credits](actions/list-person-crew-credits.md) | GET | Retrieves crew credits for a TVMaze person. |
| [List Person Crew Credits With Show](actions/list-person-crew-credits-with-show.md) | GET | Retrieves TVMaze crew credits with embedded shows. |
| [List Show Crew](actions/list-show-crew.md) | GET | Retrieves crew members for a TVMaze show. |

### Episode

| Action | Method | Description |
| --- | --- | --- |
| [Get Episode](actions/get-episode.md) | GET | Retrieves an episode from TVMaze by ID. |
| [Get Episode By Number](actions/get-episode-by-number.md) | GET | Retrieves a TVMaze episode by season and number. |
| [Get Episode With Show](actions/get-episode-with-show.md) | GET | Retrieves a TVMaze episode with its show. |
| [List Episodes By Date](actions/list-episodes-by-date.md) | GET | Retrieves TVMaze episodes for a show by airdate. |
| [List Full Schedule](actions/list-full-schedule.md) | GET | Retrieves the full schedule from TVMaze. |
| [List Schedule](actions/list-schedule.md) | GET | Retrieves the TV schedule from TVMaze. |
| [List Season Episodes](actions/list-season-episodes.md) | GET | Retrieves episodes for a TVMaze season. |
| [List Season Episodes With Guest Cast](actions/list-season-episodes-with-guest-cast.md) | GET | Retrieves TVMaze season episodes with guest cast. |
| [List Show Episodes](actions/list-show-episodes.md) | GET | Retrieves episodes for a TVMaze show. |
| [List Show Episodes With Specials](actions/list-show-episodes-with-specials.md) | GET | Retrieves all TVMaze show episodes including specials. |
| [List Web Schedule](actions/list-web-schedule.md) | GET | Retrieves the web streaming schedule from TVMaze. |

### Guest Cast Credit

| Action | Method | Description |
| --- | --- | --- |
| [List Person Guest Cast Credits With Character](actions/list-person-guest-cast-credits-with-character.md) | GET | Retrieves TVMaze guest cast credits with embedded characters. |
| [List Person Guest Cast Credits With Episode](actions/list-person-guest-cast-credits-with-episode.md) | GET | Retrieves TVMaze guest cast credits with embedded episodes. |

### Image

| Action | Method | Description |
| --- | --- | --- |
| [List Show Images](actions/list-show-images.md) | GET | Retrieves images for a TVMaze show. |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Get Person](actions/get-person.md) | GET | Retrieves a person from TVMaze by ID. |
| [Get Person With Cast Credits](actions/get-person-with-cast-credits.md) | GET | Retrieves a TVMaze person with embedded cast credits. |
| [Get Person With Crew Credits](actions/get-person-with-crew-credits.md) | GET | Retrieves a TVMaze person with embedded crew credits. |
| [Get Person With Guest Cast Credits](actions/get-person-with-guest-cast-credits.md) | GET | Retrieves a TVMaze person with embedded guest cast credits. |
| [List People](actions/list-people.md) | GET | Retrieves all person records from TVMaze. |
| [Search People](actions/search-people.md) | GET | Finds people in TVMaze by name. |

### Person Update

| Action | Method | Description |
| --- | --- | --- |
| [List Person Updates](actions/list-person-updates.md) | GET | Retrieves person update timestamps from TVMaze. |

### Season

| Action | Method | Description |
| --- | --- | --- |
| [List Show Seasons](actions/list-show-seasons.md) | GET | Retrieves seasons for a TVMaze show. |

### Show

| Action | Method | Description |
| --- | --- | --- |
| [Get Show](actions/get-show.md) | GET | Retrieves a show from TVMaze by ID. |
| [Get Show With AKAs](actions/get-show-with-akas.md) | GET | Retrieves a TVMaze show with embedded aliases. |
| [Get Show With Alternate Lists](actions/get-show-with-alternate-lists.md) | GET | Retrieves a TVMaze show with embedded alternate lists. |
| [Get Show With Cast](actions/get-show-with-cast.md) | GET | Retrieves a TVMaze show with embedded cast. |
| [Get Show With Crew](actions/get-show-with-crew.md) | GET | Retrieves a TVMaze show with embedded crew. |
| [Get Show With Episodes](actions/get-show-with-episodes.md) | GET | Retrieves a TVMaze show with embedded episodes. |
| [Get Show With Images](actions/get-show-with-images.md) | GET | Retrieves a TVMaze show with embedded images. |
| [Get Show With Next Episode](actions/get-show-with-next-episode.md) | GET | Retrieves a TVMaze show with its next episode. |
| [Get Show With Previous Episode](actions/get-show-with-previous-episode.md) | GET | Retrieves a TVMaze show with its previous episode. |
| [Get Show With Seasons](actions/get-show-with-seasons.md) | GET | Retrieves a TVMaze show with embedded seasons. |
| [List Shows](actions/list-shows.md) | GET | Retrieves all show records from TVMaze. |
| [Lookup Show By IMDb ID](actions/lookup-show-by-imdb-id.md) | GET | Finds a TVMaze show by IMDb ID. |
| [Lookup Show By TheTVDB ID](actions/lookup-show-by-thetvdb-id.md) | GET | Finds a TVMaze show by TheTVDB ID. |
| [Lookup Show By TVRage ID](actions/lookup-show-by-tvrage-id.md) | GET | Finds a TVMaze show by TVRage ID. |
| [Search Shows](actions/search-shows.md) | GET | Finds shows in TVMaze by name. |
| [Search Single Show](actions/search-single-show.md) | GET | Finds a single show in TVMaze by name. |
| [Search Single Show With Episodes](actions/search-single-show-with-episodes.md) | GET | Finds a single TVMaze show by name with episodes. |

### Show Alias

| Action | Method | Description |
| --- | --- | --- |
| [List Show AKAs](actions/list-show-akas.md) | GET | Retrieves aliases for a TVMaze show. |

### Show Update

| Action | Method | Description |
| --- | --- | --- |
| [List Show Updates](actions/list-show-updates.md) | GET | Retrieves show update timestamps from TVMaze. |

