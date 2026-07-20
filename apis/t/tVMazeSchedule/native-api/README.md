# TVMaze Schedule: Native API Reference

A consolidated summary of TVMaze Schedule's API configuration and 56 documented operations, with links to official documentation.

- **Official docs:** https://www.tvmaze.com/api
- **API base URL:** `https://api.tvmaze.com`

## Authentication

### No Authentication

TVmaze public API endpoints do not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://www.tvmaze.com/api)

## Pagination

Use `page` in the query string to choose the page; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (56 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Alternate List](actions/get-alternate-list.md) | `GET /alternatelists/{{id}}` | [docs](https://www.tvmaze.com/api#show-alternate-lists) |
| [Get Alternate List With Alternate Episodes](actions/get-alternate-list-with-alternate-episodes.md) | `GET /alternatelists/{{id}}` | [docs](https://www.tvmaze.com/api#show-alternate-lists) |
| [Get Episode](actions/get-episode.md) | `GET /episodes/{{id}}` | [docs](https://www.tvmaze.com/api#episode-main-information) |
| [Get Episode By Number](actions/get-episode-by-number.md) | `GET /shows/{{id}}/episodebynumber` | [docs](https://www.tvmaze.com/api#episode-by-number) |
| [Get Episode With Show](actions/get-episode-with-show.md) | `GET /episodes/{{id}}` | [docs](https://www.tvmaze.com/api#episode-main-information) |
| [Get Person](actions/get-person.md) | `GET /people/{{id}}` | [docs](https://www.tvmaze.com/api#person-main-information) |
| [Get Person With Cast Credits](actions/get-person-with-cast-credits.md) | `GET /people/{{id}}` | [docs](https://www.tvmaze.com/api#person-main-information) |
| [Get Person With Crew Credits](actions/get-person-with-crew-credits.md) | `GET /people/{{id}}` | [docs](https://www.tvmaze.com/api#person-main-information) |
| [Get Person With Guest Cast Credits](actions/get-person-with-guest-cast-credits.md) | `GET /people/{{id}}` | [docs](https://www.tvmaze.com/api#embedding) |
| [Get Show](actions/get-show.md) | `GET /shows/{{id}}` | [docs](https://www.tvmaze.com/api#show-main-information) |
| [Get Show With AKAs](actions/get-show-with-akas.md) | `GET /shows/{{id}}` | [docs](https://www.tvmaze.com/api#embedding) |
| [Get Show With Alternate Lists](actions/get-show-with-alternate-lists.md) | `GET /shows/{{id}}` | [docs](https://www.tvmaze.com/api#embedding) |
| [Get Show With Cast](actions/get-show-with-cast.md) | `GET /shows/{{id}}` | [docs](https://www.tvmaze.com/api#show-main-information) |
| [Get Show With Crew](actions/get-show-with-crew.md) | `GET /shows/{{id}}` | [docs](https://www.tvmaze.com/api#embedding) |
| [Get Show With Episodes](actions/get-show-with-episodes.md) | `GET /shows/{{id}}` | [docs](https://www.tvmaze.com/api#show-main-information) |
| [Get Show With Images](actions/get-show-with-images.md) | `GET /shows/{{id}}` | [docs](https://www.tvmaze.com/api#embedding) |
| [Get Show With Next Episode](actions/get-show-with-next-episode.md) | `GET /shows/{{id}}` | [docs](https://www.tvmaze.com/api#embedding) |
| [Get Show With Previous Episode](actions/get-show-with-previous-episode.md) | `GET /shows/{{id}}` | [docs](https://www.tvmaze.com/api#embedding) |
| [Get Show With Seasons](actions/get-show-with-seasons.md) | `GET /shows/{{id}}` | [docs](https://www.tvmaze.com/api#embedding) |
| [List Alternate Episodes](actions/list-alternate-episodes.md) | `GET /alternatelists/{{id}}/alternateepisodes` | [docs](https://www.tvmaze.com/api#show-alternate-lists) |
| [List Alternate Episodes With Episodes](actions/list-alternate-episodes-with-episodes.md) | `GET /alternatelists/{{id}}/alternateepisodes` | [docs](https://www.tvmaze.com/api#show-alternate-lists) |
| [List Episode Guest Cast](actions/list-episode-guest-cast.md) | `GET /episodes/{{id}}/guestcast` | [docs](https://www.tvmaze.com/api#episode-guest-cast) |
| [List Episode Guest Crew](actions/list-episode-guest-crew.md) | `GET /episodes/{{id}}/guestcrew` | [docs](https://www.tvmaze.com/api#episode-guest-crew) |
| [List Episodes By Date](actions/list-episodes-by-date.md) | `GET /shows/{{id}}/episodesbydate` | [docs](https://www.tvmaze.com/api#episodes-by-date) |
| [List Full Schedule](actions/list-full-schedule.md) | `GET /schedule/full` | [docs](https://www.tvmaze.com/api#full-schedule) |
| [List People](actions/list-people.md) | `GET /people` | [docs](https://www.tvmaze.com/api#person-index) |
| [List Person Cast Credits](actions/list-person-cast-credits.md) | `GET /people/{{id}}/castcredits` | [docs](https://www.tvmaze.com/api#person-cast-credits) |
| [List Person Cast Credits With Character](actions/list-person-cast-credits-with-character.md) | `GET /people/{{id}}/castcredits` | [docs](https://www.tvmaze.com/api#person-cast-credits) |
| [List Person Cast Credits With Show](actions/list-person-cast-credits-with-show.md) | `GET /people/{{id}}/castcredits` | [docs](https://www.tvmaze.com/api#person-cast-credits) |
| [List Person Crew Credits](actions/list-person-crew-credits.md) | `GET /people/{{id}}/crewcredits` | [docs](https://www.tvmaze.com/api#person-crew-credits) |
| [List Person Crew Credits With Show](actions/list-person-crew-credits-with-show.md) | `GET /people/{{id}}/crewcredits` | [docs](https://www.tvmaze.com/api#person-crew-credits) |
| [List Person Guest Cast Credits](actions/list-person-guest-cast-credits.md) | `GET /people/{{id}}/guestcastcredits` | [docs](https://www.tvmaze.com/api#person-guest-cast-credits) |
| [List Person Guest Cast Credits With Character](actions/list-person-guest-cast-credits-with-character.md) | `GET /people/{{id}}/guestcastcredits` | [docs](https://www.tvmaze.com/api#person-guest-cast-credits) |
| [List Person Guest Cast Credits With Episode](actions/list-person-guest-cast-credits-with-episode.md) | `GET /people/{{id}}/guestcastcredits` | [docs](https://www.tvmaze.com/api#person-guest-cast-credits) |
| [List Person Updates](actions/list-person-updates.md) | `GET /updates/people` | [docs](https://www.tvmaze.com/api#person-updates) |
| [List Schedule](actions/list-schedule.md) | `GET /schedule` | [docs](https://www.tvmaze.com/api#schedule) |
| [List Season Episodes](actions/list-season-episodes.md) | `GET /seasons/{{id}}/episodes` | [docs](https://www.tvmaze.com/api#season-episodes) |
| [List Season Episodes With Guest Cast](actions/list-season-episodes-with-guest-cast.md) | `GET /seasons/{{id}}/episodes` | [docs](https://www.tvmaze.com/api#season-episodes) |
| [List Show AKAs](actions/list-show-akas.md) | `GET /shows/{{id}}/akas` | [docs](https://www.tvmaze.com/api#show-akas) |
| [List Show Alternate Lists](actions/list-show-alternate-lists.md) | `GET /shows/{{id}}/alternatelists` | [docs](https://www.tvmaze.com/api#show-alternate-lists) |
| [List Show Cast](actions/list-show-cast.md) | `GET /shows/{{id}}/cast` | [docs](https://www.tvmaze.com/api#show-cast) |
| [List Show Crew](actions/list-show-crew.md) | `GET /shows/{{id}}/crew` | [docs](https://www.tvmaze.com/api#show-crew) |
| [List Show Episodes](actions/list-show-episodes.md) | `GET /shows/{{id}}/episodes` | [docs](https://www.tvmaze.com/api#show-episode-list) |
| [List Show Episodes With Specials](actions/list-show-episodes-with-specials.md) | `GET /shows/{{id}}/episodes` | [docs](https://www.tvmaze.com/api#show-episode-list) |
| [List Show Images](actions/list-show-images.md) | `GET /shows/{{id}}/images` | [docs](https://www.tvmaze.com/api#show-images) |
| [List Show Seasons](actions/list-show-seasons.md) | `GET /shows/{{id}}/seasons` | [docs](https://www.tvmaze.com/api#show-seasons) |
| [List Show Updates](actions/list-show-updates.md) | `GET /updates/shows` | [docs](https://www.tvmaze.com/api#show-updates) |
| [List Shows](actions/list-shows.md) | `GET /shows` | [docs](https://www.tvmaze.com/api#show-index) |
| [List Web Schedule](actions/list-web-schedule.md) | `GET /schedule/web` | [docs](https://www.tvmaze.com/api#web-streaming-schedule) |
| [Lookup Show By IMDb ID](actions/lookup-show-by-imdb-id.md) | `GET /lookup/shows` | [docs](https://www.tvmaze.com/api#show-lookup) |
| [Lookup Show By TheTVDB ID](actions/lookup-show-by-thetvdb-id.md) | `GET /lookup/shows` | [docs](https://www.tvmaze.com/api#show-lookup) |
| [Lookup Show By TVRage ID](actions/lookup-show-by-tvrage-id.md) | `GET /lookup/shows` | [docs](https://www.tvmaze.com/api#show-lookup) |
| [Search People](actions/search-people.md) | `GET /search/people` | [docs](https://www.tvmaze.com/api#people-search) |
| [Search Shows](actions/search-shows.md) | `GET /search/shows` | [docs](https://www.tvmaze.com/api#show-search) |
| [Search Single Show](actions/search-single-show.md) | `GET /singlesearch/shows` | [docs](https://www.tvmaze.com/api#show-single-search) |
| [Search Single Show With Episodes](actions/search-single-show-with-episodes.md) | `GET /singlesearch/shows` | [docs](https://www.tvmaze.com/api#show-single-search) |
