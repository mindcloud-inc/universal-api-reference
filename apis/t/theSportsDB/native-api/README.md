# TheSportsDB: Native API Reference

A consolidated summary of TheSportsDB's API configuration and 37 documented operations, with links to official documentation.

- **Official docs:** https://www.thesportsdb.com/documentation
- **API base URL:** `https://www.thesportsdb.com/api/v1/json/123`

## Authentication

### No Authentication

The free TheSportsDB v1 API is publicly accessible with the documented shared key embedded in the base URL, so no tenant credential is required.

This API does not require request authentication.

[Official authentication documentation](https://www.thesportsdb.com/documentation)

## Endpoints (37 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Event](actions/get-event.md) | `GET /lookupevent.php` | [docs](https://www.thesportsdb.com/documentation) |
| [Get League](actions/get-league.md) | `GET /lookupleague.php` | [docs](https://www.thesportsdb.com/documentation) |
| [Get League Table](actions/get-league-table.md) | `GET /lookuptable.php` | [docs](https://www.thesportsdb.com/documentation) |
| [Get Player](actions/get-player.md) | `GET /lookupplayer.php` | [docs](https://www.thesportsdb.com/documentation) |
| [Get Team](actions/get-team.md) | `GET /lookupteam.php` | [docs](https://www.thesportsdb.com/documentation) |
| [Get Team Equipment](actions/get-team-equipment.md) | `GET /lookupequipment.php` | [docs](https://www.thesportsdb.com/documentation) |
| [Get Venue](actions/get-venue.md) | `GET /lookupvenue.php` | [docs](https://www.thesportsdb.com/documentation) |
| [List All Countries](actions/list-all-countries.md) | `GET /all_countries.php` | [docs](https://www.thesportsdb.com/documentation) |
| [List All Leagues](actions/list-all-leagues.md) | `GET /all_leagues.php` | [docs](https://www.thesportsdb.com/documentation) |
| [List All Sports](actions/list-all-sports.md) | `GET /all_sports.php` | [docs](https://www.thesportsdb.com/documentation) |
| [List Event Highlights By Day](actions/list-event-highlights-by-day.md) | `GET /eventshighlights.php` | [docs](https://www.thesportsdb.com/documentation) |
| [List Event Lineup](actions/list-event-lineup.md) | `GET /lookuplineup.php` | [docs](https://www.thesportsdb.com/documentation) |
| [List Event Results](actions/list-event-results.md) | `GET /eventresults.php` | [docs](https://www.thesportsdb.com/documentation) |
| [List Event Statistics](actions/list-event-statistics.md) | `GET /lookupeventstats.php` | [docs](https://www.thesportsdb.com/documentation) |
| [List Event Timeline](actions/list-event-timeline.md) | `GET /lookuptimeline.php` | [docs](https://www.thesportsdb.com/documentation) |
| [List Events By Day](actions/list-events-by-day.md) | `GET /eventsday.php` | [docs](https://www.thesportsdb.com/documentation) |
| [List League Season Events](actions/list-league-season-events.md) | `GET /eventsseason.php` | [docs](https://www.thesportsdb.com/documentation) |
| [List League Seasons](actions/list-league-seasons.md) | `GET /search_all_seasons.php` | [docs](https://www.thesportsdb.com/documentation) |
| [List Leagues By Country And Sport](actions/list-leagues-by-country-and-sport.md) | `GET /search_all_leagues.php` | [docs](https://www.thesportsdb.com/documentation) |
| [List Next League Events](actions/list-next-league-events.md) | `GET /eventsnextleague.php` | [docs](https://www.thesportsdb.com/documentation) |
| [List Next Team Events](actions/list-next-team-events.md) | `GET /eventsnext.php` | [docs](https://www.thesportsdb.com/documentation) |
| [List Player Contracts](actions/list-player-contracts.md) | `GET /lookupcontracts.php` | [docs](https://www.thesportsdb.com/documentation) |
| [List Player Former Teams](actions/list-player-former-teams.md) | `GET /lookupformerteams.php` | [docs](https://www.thesportsdb.com/documentation) |
| [List Player Honours](actions/list-player-honours.md) | `GET /lookuphonours.php` | [docs](https://www.thesportsdb.com/documentation) |
| [List Player Milestones](actions/list-player-milestones.md) | `GET /lookupmilestones.php` | [docs](https://www.thesportsdb.com/documentation) |
| [List Player Results](actions/list-player-results.md) | `GET /playerresults.php` | [docs](https://www.thesportsdb.com/documentation) |
| [List Previous League Events](actions/list-previous-league-events.md) | `GET /eventspastleague.php` | [docs](https://www.thesportsdb.com/documentation) |
| [List Previous Team Events](actions/list-previous-team-events.md) | `GET /eventslast.php` | [docs](https://www.thesportsdb.com/documentation) |
| [List Team Players](actions/list-team-players.md) | `GET /lookup_all_players.php` | [docs](https://www.thesportsdb.com/documentation) |
| [List Teams By League Name](actions/list-teams-by-league-name.md) | `GET /search_all_teams.php` | [docs](https://www.thesportsdb.com/documentation) |
| [List Teams By Sport And Country](actions/list-teams-by-sport-and-country.md) | `GET /search_all_teams.php` | [docs](https://www.thesportsdb.com/documentation) |
| [List TV Events](actions/list-tv-events.md) | `GET /eventstv.php` | [docs](https://www.thesportsdb.com/documentation) |
| [Search Events](actions/search-events.md) | `GET /searchevents.php` | [docs](https://www.thesportsdb.com/documentation) |
| [Search Events By Filename](actions/search-events-by-filename.md) | `GET /searchevents.php` | [docs](https://www.thesportsdb.com/documentation) |
| [Search Players](actions/search-players.md) | `GET /searchplayers.php` | [docs](https://www.thesportsdb.com/documentation) |
| [Search Teams](actions/search-teams.md) | `GET /searchteams.php` | [docs](https://www.thesportsdb.com/documentation) |
| [Search Venues](actions/search-venues.md) | `GET /searchvenues.php` | [docs](https://www.thesportsdb.com/documentation) |
