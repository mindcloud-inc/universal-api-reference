# <img src="https://images.mindcloud.co/apps/icons/the-sports-db_1776175681678.png" alt="TheSportsDB logo" width="28" height="28"> TheSportsDB: Universal API

Access public sports data from TheSportsDB, including leagues, teams, players, events, venues, standings, schedules, and TV listings from the free v1 API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/theSportsDB/latest
- **Actions:** 37
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.thesportsdb.com/
- **Vendor API docs:** https://www.thesportsdb.com/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List All Sports](actions/list-all-sports.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/theSportsDB/latest/actions/list-all-sports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (37)

### Country

| Action | Method | Description |
| --- | --- | --- |
| [List All Countries](actions/list-all-countries.md) | GET | Retrieves all supported countries from TheSportsDB. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from TheSportsDB by ID. |
| [List Events By Day](actions/list-events-by-day.md) | GET | Retrieves events in TheSportsDB for a specific day. |
| [List League Season Events](actions/list-league-season-events.md) | GET | Retrieves league events in TheSportsDB by season. |
| [List Next League Events](actions/list-next-league-events.md) | GET | Retrieves upcoming events for a league in TheSportsDB. |
| [List Next Team Events](actions/list-next-team-events.md) | GET | Retrieves upcoming events for a team in TheSportsDB. |
| [List Previous League Events](actions/list-previous-league-events.md) | GET | Retrieves recent events for a league in TheSportsDB. |
| [List Previous Team Events](actions/list-previous-team-events.md) | GET | Retrieves recent events for a team in TheSportsDB. |
| [Search Events](actions/search-events.md) | GET | Finds events in TheSportsDB by event name. |
| [Search Events By Filename](actions/search-events-by-filename.md) | GET | Finds events in TheSportsDB by event filename. |

### Event Highlight

| Action | Method | Description |
| --- | --- | --- |
| [List Event Highlights By Day](actions/list-event-highlights-by-day.md) | GET | Retrieves event highlights in TheSportsDB for a specific day. |

### Event Lineup Entry

| Action | Method | Description |
| --- | --- | --- |
| [List Event Lineup](actions/list-event-lineup.md) | GET | Retrieves event lineups from TheSportsDB by event ID. |

### Event Result

| Action | Method | Description |
| --- | --- | --- |
| [List Event Results](actions/list-event-results.md) | GET | Retrieves event results from TheSportsDB by event ID. |

### Event Statistic

| Action | Method | Description |
| --- | --- | --- |
| [List Event Statistics](actions/list-event-statistics.md) | GET | Retrieves event statistics from TheSportsDB by event ID. |

### Event Timeline Entry

| Action | Method | Description |
| --- | --- | --- |
| [List Event Timeline](actions/list-event-timeline.md) | GET | Retrieves event timeline entries from TheSportsDB by event ID. |

### Former Team

| Action | Method | Description |
| --- | --- | --- |
| [List Player Former Teams](actions/list-player-former-teams.md) | GET | Retrieves former teams for a player in TheSportsDB. |

### League

| Action | Method | Description |
| --- | --- | --- |
| [Get League](actions/get-league.md) | GET | Retrieves a league from TheSportsDB by ID. |
| [List All Leagues](actions/list-all-leagues.md) | GET | Retrieves all leagues listed in TheSportsDB. |
| [List Leagues By Country And Sport](actions/list-leagues-by-country-and-sport.md) | GET | Retrieves leagues in TheSportsDB by country and sport. |

### League Table Row

| Action | Method | Description |
| --- | --- | --- |
| [Get League Table](actions/get-league-table.md) | GET | Retrieves a league table from TheSportsDB by league and season. |

### Player

| Action | Method | Description |
| --- | --- | --- |
| [Get Player](actions/get-player.md) | GET | Retrieves a player from TheSportsDB by ID. |
| [List Team Players](actions/list-team-players.md) | GET | Retrieves players for a team in TheSportsDB. |
| [Search Players](actions/search-players.md) | GET | Finds players in TheSportsDB by player name. |

### Player Contract

| Action | Method | Description |
| --- | --- | --- |
| [List Player Contracts](actions/list-player-contracts.md) | GET | Retrieves player contracts from TheSportsDB by player ID. |

### Player Honour

| Action | Method | Description |
| --- | --- | --- |
| [List Player Honours](actions/list-player-honours.md) | GET | Retrieves player honours from TheSportsDB by player ID. |

### Player Milestone

| Action | Method | Description |
| --- | --- | --- |
| [List Player Milestones](actions/list-player-milestones.md) | GET | Retrieves player milestones from TheSportsDB by player ID. |

### Player Result

| Action | Method | Description |
| --- | --- | --- |
| [List Player Results](actions/list-player-results.md) | GET | Retrieves player results from TheSportsDB by player ID. |

### Season

| Action | Method | Description |
| --- | --- | --- |
| [List League Seasons](actions/list-league-seasons.md) | GET | Retrieves league seasons from TheSportsDB by league ID. |

### Sport

| Action | Method | Description |
| --- | --- | --- |
| [List All Sports](actions/list-all-sports.md) | GET | Retrieves all sport categories from TheSportsDB. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Get Team](actions/get-team.md) | GET | Retrieves a team from TheSportsDB by ID. |
| [List Teams By League Name](actions/list-teams-by-league-name.md) | GET | Retrieves teams in TheSportsDB by league name. |
| [List Teams By Sport And Country](actions/list-teams-by-sport-and-country.md) | GET | Retrieves teams in TheSportsDB by sport and country. |
| [Search Teams](actions/search-teams.md) | GET | Finds teams in TheSportsDB by team name. |

### Team Equipment

| Action | Method | Description |
| --- | --- | --- |
| [Get Team Equipment](actions/get-team-equipment.md) | GET | Retrieves team equipment from TheSportsDB by team ID. |

### Tv Event

| Action | Method | Description |
| --- | --- | --- |
| [List TV Events](actions/list-tv-events.md) | GET | Retrieves televised events in TheSportsDB for a specific day. |

### Venue

| Action | Method | Description |
| --- | --- | --- |
| [Get Venue](actions/get-venue.md) | GET | Retrieves a venue from TheSportsDB by ID. |
| [Search Venues](actions/search-venues.md) | GET | Finds venues in TheSportsDB by venue name. |

