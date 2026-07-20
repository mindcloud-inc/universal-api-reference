# College Football Data: Native API Reference

A consolidated summary of College Football Data's API configuration and 60 documented operations, with links to official documentation.

- **Official docs:** https://api.collegefootballdata.com/
- **OpenAPI specification:** https://api.collegefootballdata.com/swagger-ui-init.js
- **API base URL:** `https://api.collegefootballdata.com`

## Authentication

### API Key

Use a College Football Data API key. MindCloud sends it as Authorization: Bearer <apiKey>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.collegefootballdata.com/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (60 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Adjusted Player Passing Stats](actions/get-adjusted-player-passing-stats.md) | `GET /wepa/players/passing` | [docs](https://api.collegefootballdata.com/) |
| [List Adjusted Player Rushing Stats](actions/get-adjusted-player-rushing-stats.md) | `GET /wepa/players/rushing` | [docs](https://api.collegefootballdata.com/) |
| [List Adjusted Team Season Stats](actions/get-adjusted-team-season-stats.md) | `GET /wepa/team/season` | [docs](https://api.collegefootballdata.com/) |
| [Get Advanced Box Score](actions/get-advanced-box-score.md) | `GET /game/box/advanced` | [docs](https://api.collegefootballdata.com/) |
| [List Advanced Game Stats](actions/get-advanced-game-stats.md) | `GET /stats/game/advanced` | [docs](https://api.collegefootballdata.com/) |
| [List Advanced Season Stats](actions/get-advanced-season-stats.md) | `GET /stats/season/advanced` | [docs](https://api.collegefootballdata.com/) |
| [List Aggregated Team Recruiting Ratings](actions/get-aggregated-team-recruiting-ratings.md) | `GET /recruiting/groups` | [docs](https://api.collegefootballdata.com/) |
| [List Calendar](actions/get-calendar.md) | `GET /calendar` | [docs](https://api.collegefootballdata.com/) |
| [List Categories](actions/get-categories.md) | `GET /stats/categories` | [docs](https://api.collegefootballdata.com/) |
| [List Coaches](actions/get-coaches.md) | `GET /coaches` | [docs](https://api.collegefootballdata.com/) |
| [List Conference S P](actions/get-conference-sp.md) | `GET /ratings/sp/conferences` | [docs](https://api.collegefootballdata.com/) |
| [List Conferences](actions/get-conferences.md) | `GET /conferences` | [docs](https://api.collegefootballdata.com/) |
| [List Draft Picks](actions/get-draft-picks.md) | `GET /draft/picks` | [docs](https://api.collegefootballdata.com/) |
| [List Draft Positions](actions/get-draft-positions.md) | `GET /draft/positions` | [docs](https://api.collegefootballdata.com/) |
| [List Draft Teams](actions/get-draft-teams.md) | `GET /draft/teams` | [docs](https://api.collegefootballdata.com/) |
| [List Drives](actions/get-drives.md) | `GET /drives` | [docs](https://api.collegefootballdata.com/) |
| [List Elo](actions/get-elo.md) | `GET /ratings/elo` | [docs](https://api.collegefootballdata.com/) |
| [List F B S Teams](actions/get-fbs-teams.md) | `GET /teams/fbs` | [docs](https://api.collegefootballdata.com/) |
| [List Field Goal Expected Points](actions/get-field-goal-expected-points.md) | `GET /metrics/fg/ep` | [docs](https://api.collegefootballdata.com/) |
| [List F P I](actions/get-fpi.md) | `GET /ratings/fpi` | [docs](https://api.collegefootballdata.com/) |
| [List Game Havoc Stats](actions/get-game-havoc-stats.md) | `GET /stats/game/havoc` | [docs](https://api.collegefootballdata.com/) |
| [List Game Player Stats](actions/get-game-player-stats.md) | `GET /games/players` | [docs](https://api.collegefootballdata.com/) |
| [List Game Team Stats](actions/get-game-team-stats.md) | `GET /games/teams` | [docs](https://api.collegefootballdata.com/) |
| [List Games](actions/get-games.md) | `GET /games` | [docs](https://api.collegefootballdata.com/) |
| [List Kicker Paar](actions/get-kicker-paar.md) | `GET /wepa/players/kicking` | [docs](https://api.collegefootballdata.com/) |
| [List Lines](actions/get-lines.md) | `GET /lines` | [docs](https://api.collegefootballdata.com/) |
| [Get Live Plays](actions/get-live-plays.md) | `GET /live/plays` | [docs](https://api.collegefootballdata.com/) |
| [Get Matchup](actions/get-matchup.md) | `GET /teams/matchup` | [docs](https://api.collegefootballdata.com/) |
| [List Media](actions/get-media.md) | `GET /games/media` | [docs](https://api.collegefootballdata.com/) |
| [List Play Stat Types](actions/get-play-stat-types.md) | `GET /plays/stats/types` | [docs](https://api.collegefootballdata.com/) |
| [List Play Stats](actions/get-play-stats.md) | `GET /plays/stats` | [docs](https://api.collegefootballdata.com/) |
| [List Play Types](actions/get-play-types.md) | `GET /plays/types` | [docs](https://api.collegefootballdata.com/) |
| [List Player Season Stats](actions/get-player-season-stats.md) | `GET /stats/player/season` | [docs](https://api.collegefootballdata.com/) |
| [List Player Usage](actions/get-player-usage.md) | `GET /player/usage` | [docs](https://api.collegefootballdata.com/) |
| [List Plays](actions/get-plays.md) | `GET /plays` | [docs](https://api.collegefootballdata.com/) |
| [List Predicted Points](actions/get-predicted-points.md) | `GET /ppa/predicted` | [docs](https://api.collegefootballdata.com/) |
| [List Predicted Points Added By Game](actions/get-predicted-points-added-by-game.md) | `GET /ppa/games` | [docs](https://api.collegefootballdata.com/) |
| [List Predicted Points Added By Player Game](actions/get-predicted-points-added-by-player-game.md) | `GET /ppa/players/games` | [docs](https://api.collegefootballdata.com/) |
| [List Predicted Points Added By Player Season](actions/get-predicted-points-added-by-player-season.md) | `GET /ppa/players/season` | [docs](https://api.collegefootballdata.com/) |
| [List Predicted Points Added By Team](actions/get-predicted-points-added-by-team.md) | `GET /ppa/teams` | [docs](https://api.collegefootballdata.com/) |
| [List Pregame Win Probabilities](actions/get-pregame-win-probabilities.md) | `GET /metrics/wp/pregame` | [docs](https://api.collegefootballdata.com/) |
| [List Rankings](actions/get-rankings.md) | `GET /rankings` | [docs](https://api.collegefootballdata.com/) |
| [List Records](actions/get-records.md) | `GET /records` | [docs](https://api.collegefootballdata.com/) |
| [List Recruits](actions/get-recruits.md) | `GET /recruiting/players` | [docs](https://api.collegefootballdata.com/) |
| [List Returning Production](actions/get-returning-production.md) | `GET /player/returning` | [docs](https://api.collegefootballdata.com/) |
| [List Roster](actions/get-roster.md) | `GET /roster` | [docs](https://api.collegefootballdata.com/) |
| [List Scoreboard](actions/get-scoreboard.md) | `GET /scoreboard` | [docs](https://api.collegefootballdata.com/) |
| [List S P](actions/get-sp.md) | `GET /ratings/sp` | [docs](https://api.collegefootballdata.com/) |
| [List S R S](actions/get-srs.md) | `GET /ratings/srs` | [docs](https://api.collegefootballdata.com/) |
| [List Talent](actions/get-talent.md) | `GET /talent` | [docs](https://api.collegefootballdata.com/) |
| [List Team Recruiting Rankings](actions/get-team-recruiting-rankings.md) | `GET /recruiting/teams` | [docs](https://api.collegefootballdata.com/) |
| [List Team Stats](actions/get-team-stats.md) | `GET /stats/season` | [docs](https://api.collegefootballdata.com/) |
| [List Teams](actions/get-teams.md) | `GET /teams` | [docs](https://api.collegefootballdata.com/) |
| [List Teams A T S](actions/get-teams-ats.md) | `GET /teams/ats` | [docs](https://api.collegefootballdata.com/) |
| [List Transfer Portal](actions/get-transfer-portal.md) | `GET /player/portal` | [docs](https://api.collegefootballdata.com/) |
| [Get User Info](actions/get-user-info.md) | `GET /info` | [docs](https://api.collegefootballdata.com/) |
| [List Venues](actions/get-venues.md) | `GET /venues` | [docs](https://api.collegefootballdata.com/) |
| [List Weather](actions/get-weather.md) | `GET /games/weather` | [docs](https://api.collegefootballdata.com/) |
| [List Win Probability](actions/get-win-probability.md) | `GET /metrics/wp` | [docs](https://api.collegefootballdata.com/) |
| [Search Players](actions/search-players.md) | `GET /player/search` | [docs](https://api.collegefootballdata.com/) |
