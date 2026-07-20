# SportsData: Native API Reference

A consolidated summary of SportsData's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://sportsdata.io/developers
- **API base URL:** `https://api.sportsdata.io`

## Authentication

### API Key

Connect with a SportsDataIO API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://sportsdata.io/developers/apis)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [NBA Team Profiles](actions/n-ba-team-profiles.md) | `GET /v3/nba/scores/json/teams` | [docs](https://cdn.sportsdata.io/openapi/NBA-openapi-3.1.json) |
| [NFL Team Profiles](actions/n-fl-team-profiles.md) | `GET /v3/nfl/scores/json/Teams` | [docs](https://cdn.sportsdata.io/openapi/NFL-openapi-3.1.json) |
| [NBA Active Players Basic](actions/nba-active-players-basic.md) | `GET /v3/nba/scores/json/PlayersActiveBasic` | [docs](https://cdn.sportsdata.io/openapi/NBA-openapi-3.1.json) |
| [NBA Current Season](actions/nba-current-season.md) | `GET /v3/nba/scores/json/CurrentSeason` | [docs](https://cdn.sportsdata.io/openapi/NBA-openapi-3.1.json) |
| [NBA Free Agents](actions/nba-free-agents.md) | `GET /v3/nba/scores/json/PlayersByFreeAgents` | [docs](https://cdn.sportsdata.io/openapi/NBA-openapi-3.1.json) |
| [NBA Games By Date](actions/nba-games-by-date.md) | `GET /v3/nba/scores/json/GamesByDate/:date` | [docs](https://cdn.sportsdata.io/openapi/NBA-openapi-3.1.json) |
| [NBA Games By Season](actions/nba-games-by-season.md) | `GET /v3/nba/scores/json/Games/:season` | [docs](https://cdn.sportsdata.io/openapi/NBA-openapi-3.1.json) |
| [NBA News](actions/nba-news.md) | `GET /v3/nba/scores/json/News` | [docs](https://cdn.sportsdata.io/openapi/NBA-openapi-3.1.json) |
| [NBA Players](actions/nba-players.md) | `GET /v3/nba/scores/json/Players` | [docs](https://cdn.sportsdata.io/openapi/NBA-openapi-3.1.json) |
| [NBA Referees](actions/nba-referees.md) | `GET /v3/nba/scores/json/Referees` | [docs](https://cdn.sportsdata.io/openapi/NBA-openapi-3.1.json) |
| [NBA Stadiums](actions/nba-stadiums.md) | `GET /v3/nba/scores/json/Stadiums` | [docs](https://cdn.sportsdata.io/openapi/NBA-openapi-3.1.json) |
| [NBA Standings](actions/nba-standings.md) | `GET /v3/nba/scores/json/Standings/:season` | [docs](https://cdn.sportsdata.io/openapi/NBA-openapi-3.1.json) |
| [NFL Current Season](actions/nfl-current-season.md) | `GET /v3/nfl/scores/json/CurrentSeason` | [docs](https://cdn.sportsdata.io/openapi/NFL-openapi-3.1.json) |
| [NFL Current Week](actions/nfl-current-week.md) | `GET /v3/nfl/scores/json/CurrentWeek` | [docs](https://cdn.sportsdata.io/openapi/NFL-openapi-3.1.json) |
| [NFL Free Agents](actions/nfl-free-agents.md) | `GET /v3/nfl/scores/json/FreeAgents` | [docs](https://cdn.sportsdata.io/openapi/NFL-openapi-3.1.json) |
| [NFL News](actions/nfl-news.md) | `GET /v3/nfl/scores/json/News` | [docs](https://cdn.sportsdata.io/openapi/NFL-openapi-3.1.json) |
| [NFL News By Team](actions/nfl-news-by-team.md) | `GET /v3/nfl/scores/json/NewsByTeam/:team` | [docs](https://cdn.sportsdata.io/openapi/NFL-openapi-3.1.json) |
| [NFL Players](actions/nfl-players.md) | `GET /v3/nfl/scores/json/Players` | [docs](https://cdn.sportsdata.io/openapi/NFL-openapi-3.1.json) |
| [NFL Players By Team](actions/nfl-players-by-team.md) | `GET /v3/nfl/scores/json/Players/:team` | [docs](https://cdn.sportsdata.io/openapi/NFL-openapi-3.1.json) |
| [NFL Referees](actions/nfl-referees.md) | `GET /v3/nfl/scores/json/Referees` | [docs](https://cdn.sportsdata.io/openapi/NFL-openapi-3.1.json) |
| [NFL Schedules By Season](actions/nfl-schedules-by-season.md) | `GET /v3/nfl/scores/json/Schedules/:season` | [docs](https://cdn.sportsdata.io/openapi/NFL-openapi-3.1.json) |
| [NFL Scores By Week](actions/nfl-scores-by-week.md) | `GET /v3/nfl/scores/json/ScoresByWeek/:season/:week` | [docs](https://cdn.sportsdata.io/openapi/NFL-openapi-3.1.json) |
| [NFL Stadiums](actions/nfl-stadiums.md) | `GET /v3/nfl/scores/json/Stadiums` | [docs](https://cdn.sportsdata.io/openapi/NFL-openapi-3.1.json) |
| [NFL Standings](actions/nfl-standings.md) | `GET /v3/nfl/scores/json/Standings/:season` | [docs](https://cdn.sportsdata.io/openapi/NFL-openapi-3.1.json) |
