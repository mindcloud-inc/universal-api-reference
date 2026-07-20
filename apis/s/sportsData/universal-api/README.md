# <img src="https://images.mindcloud.co/apps/icons/sports-data_1775752893224.png" alt="SportsData logo" width="28" height="28"> SportsData: Universal API

Access SportsDataIO sports data APIs for schedules, scores, standings, teams, players, odds, and related league data across supported sports.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sportsData/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sportsdata.io
- **Vendor API docs:** https://sportsdata.io/developers

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [NFL Team Profiles](actions/n-fl-team-profiles.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/n-fl-team-profiles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Game

| Action | Method | Description |
| --- | --- | --- |
| [NBA Games By Date](actions/nba-games-by-date.md) | GET | Retrieves NBA games from SportsData by date. |
| [NBA Games By Season](actions/nba-games-by-season.md) | GET | Retrieves NBA games from SportsData by season. |
| [NFL Schedules By Season](actions/nfl-schedules-by-season.md) | GET | Retrieves NFL schedules from SportsData by season. |
| [NFL Scores By Week](actions/nfl-scores-by-week.md) | GET | Retrieves NFL scores from SportsData by week. |

### News

| Action | Method | Description |
| --- | --- | --- |
| [NBA News](actions/nba-news.md) | GET | Retrieves NBA news from SportsData. |
| [NFL News](actions/nfl-news.md) | GET | Retrieves NFL news from SportsData. |
| [NFL News By Team](actions/nfl-news-by-team.md) | GET | Retrieves NFL news from SportsData by team. |

### Player

| Action | Method | Description |
| --- | --- | --- |
| [NBA Active Players Basic](actions/nba-active-players-basic.md) | GET | Retrieves active NBA player profiles from SportsData. |
| [NBA Free Agents](actions/nba-free-agents.md) | GET | Retrieves NBA free agents from SportsData. |
| [NBA Players](actions/nba-players.md) | GET | Retrieves active NBA player details from SportsData. |
| [NFL Free Agents](actions/nfl-free-agents.md) | GET | Retrieves NFL free agents from SportsData. |
| [NFL Players](actions/nfl-players.md) | GET | Retrieves NFL player details from SportsData. |
| [NFL Players By Team](actions/nfl-players-by-team.md) | GET | Retrieves NFL player details from SportsData by team. |

### Referee

| Action | Method | Description |
| --- | --- | --- |
| [NBA Referees](actions/nba-referees.md) | GET | Retrieves NBA referees from SportsData. |
| [NFL Referees](actions/nfl-referees.md) | GET | Retrieves NFL referees from SportsData. |

### Season

| Action | Method | Description |
| --- | --- | --- |
| [NBA Current Season](actions/nba-current-season.md) | GET | Retrieves the current NBA season from SportsData. |
| [NFL Current Season](actions/nfl-current-season.md) | GET | Retrieves the current NFL season from SportsData. |

### Stadium

| Action | Method | Description |
| --- | --- | --- |
| [NBA Stadiums](actions/nba-stadiums.md) | GET | Retrieves NBA stadiums from SportsData. |
| [NFL Stadiums](actions/nfl-stadiums.md) | GET | Retrieves NFL stadiums from SportsData. |

### Standing

| Action | Method | Description |
| --- | --- | --- |
| [NBA Standings](actions/nba-standings.md) | GET | Retrieves NBA standings from SportsData. |
| [NFL Standings](actions/nfl-standings.md) | GET | Retrieves NFL standings from SportsData. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [NBA Team Profiles](actions/n-ba-team-profiles.md) | GET | Retrieves active NBA team profiles from SportsData. |
| [NFL Team Profiles](actions/n-fl-team-profiles.md) | GET | Retrieves active NFL team profiles from SportsData. |

### Week

| Action | Method | Description |
| --- | --- | --- |
| [NFL Current Week](actions/nfl-current-week.md) | GET | Retrieves the current NFL week from SportsData. |

