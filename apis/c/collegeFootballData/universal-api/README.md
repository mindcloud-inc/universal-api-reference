# <img src="https://images.mindcloud.co/apps/icons/college-football-data-icon_1775759081778.png" alt="College Football Data logo" width="28" height="28"> College Football Data: Universal API

Official College Football Data API for teams, games, rankings, recruiting, ratings, play-by-play, advanced metrics, and live college football data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/collegeFootballData/latest
- **Actions:** 60
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://collegefootballdata.com
- **Vendor API docs:** https://api.collegefootballdata.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Info](actions/get-user-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (60)

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [List Categories](actions/get-categories.md) | GET | Retrieves team statistical categories from College Football Data. |
| [List Play Stat Types](actions/get-play-stat-types.md) | GET | Retrieves play stat types from College Football Data. |
| [List Play Types](actions/get-play-types.md) | GET | Retrieves play types from College Football Data. |

### Drives

| Action | Method | Description |
| --- | --- | --- |
| [List Drives](actions/get-drives.md) | GET | Retrieves historical drives from College Football Data. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [List Advanced Game Stats](actions/get-advanced-game-stats.md) | GET | Retrieves advanced game statistics from College Football Data. |
| [List Game Havoc Stats](actions/get-game-havoc-stats.md) | GET | Retrieves game havoc statistics from College Football Data. |
| [List Game Player Stats](actions/get-game-player-stats.md) | GET | Retrieves player box score statistics from College Football Data. |
| [List Game Team Stats](actions/get-game-team-stats.md) | GET | Retrieves team box score statistics from College Football Data. |
| [List Games](actions/get-games.md) | GET | Retrieves historical games from College Football Data. |
| [Get Live Plays](actions/get-live-plays.md) | GET | Retrieves live play-by-play data from College Football Data. |
| [List Media](actions/get-media.md) | GET | Retrieves game media information from College Football Data. |
| [List Play Stats](actions/get-play-stats.md) | GET | Retrieves player-play associations from College Football Data. |
| [List Plays](actions/get-plays.md) | GET | Retrieves historical plays from College Football Data. |
| [List Predicted Points Added By Game](actions/get-predicted-points-added-by-game.md) | GET | Retrieves team PPA metrics by game from College Football Data. |
| [List Scoreboard](actions/get-scoreboard.md) | GET | Retrieves live scoreboard data from College Football Data. |
| [List Weather](actions/get-weather.md) | GET | Retrieves game weather data from College Football Data. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [List Adjusted Player Passing Stats](actions/get-adjusted-player-passing-stats.md) | GET | Retrieves opponent-adjusted player passing statistics from College Football Data. |
| [List Adjusted Player Rushing Stats](actions/get-adjusted-player-rushing-stats.md) | GET | Retrieves opponent-adjusted player rushing statistics from College Football Data. |
| [List Conferences](actions/get-conferences.md) | GET | Retrieves conferences from College Football Data. |
| [List Draft Picks](actions/get-draft-picks.md) | GET | Retrieves historical NFL draft picks from College Football Data. |
| [List Kicker Paar](actions/get-kicker-paar.md) | GET | Retrieves kicker PAAR ratings from College Football Data. |
| [List Player Season Stats](actions/get-player-season-stats.md) | GET | Retrieves player season statistics from College Football Data. |
| [List Player Usage](actions/get-player-usage.md) | GET | Retrieves player usage data from College Football Data. |
| [List Predicted Points Added By Player Game](actions/get-predicted-points-added-by-player-game.md) | GET | Retrieves player PPA statistics by game from College Football Data. |
| [List Predicted Points Added By Player Season](actions/get-predicted-points-added-by-player-season.md) | GET | Retrieves player PPA statistics by season from College Football Data. |
| [List Recruits](actions/get-recruits.md) | GET | Retrieves player recruiting rankings from College Football Data. |
| [List Returning Production](actions/get-returning-production.md) | GET | Retrieves returning production data from College Football Data. |
| [List Roster](actions/get-roster.md) | GET | Retrieves historical team rosters from College Football Data. |
| [List Transfer Portal](actions/get-transfer-portal.md) | GET | Retrieves transfer portal entries from College Football Data. |
| [Search Players](actions/search-players.md) | GET | Finds players in College Football Data by name. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [List Venues](actions/get-venues.md) | GET | Retrieves venues from College Football Data. |

### Metrics

| Action | Method | Description |
| --- | --- | --- |
| [List Field Goal Expected Points](actions/get-field-goal-expected-points.md) | GET | Retrieves field goal expected points from College Football Data. |
| [List Predicted Points](actions/get-predicted-points.md) | GET | Retrieves predicted points by down and distance from College Football Data. |
| [List Pregame Win Probabilities](actions/get-pregame-win-probabilities.md) | GET | Retrieves pregame win probabilities from College Football Data. |
| [List Win Probability](actions/get-win-probability.md) | GET | Retrieves play win probabilities from College Football Data. |

### Positions

| Action | Method | Description |
| --- | --- | --- |
| [List Draft Positions](actions/get-draft-positions.md) | GET | Retrieves NFL draft position categories from College Football Data. |

### Prices

| Action | Method | Description |
| --- | --- | --- |
| [List Lines](actions/get-lines.md) | GET | Retrieves historical betting lines from College Football Data. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Advanced Box Score](actions/get-advanced-box-score.md) | GET | Retrieves an advanced box score from College Football Data. |
| [List Aggregated Team Recruiting Ratings](actions/get-aggregated-team-recruiting-ratings.md) | GET | Retrieves aggregated team recruiting ratings from College Football Data. |
| [List Conference S P](actions/get-conference-sp.md) | GET | Retrieves conference SP+ data from College Football Data. |
| [List Rankings](actions/get-rankings.md) | GET | Retrieves historical poll rankings from College Football Data. |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [List Calendar](actions/get-calendar.md) | GET | Retrieves season calendar information from College Football Data. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [List Adjusted Team Season Stats](actions/get-adjusted-team-season-stats.md) | GET | Retrieves opponent-adjusted team season statistics from College Football Data. |
| [List Advanced Season Stats](actions/get-advanced-season-stats.md) | GET | Retrieves advanced team season statistics from College Football Data. |
| [List Draft Teams](actions/get-draft-teams.md) | GET | Retrieves NFL teams from College Football Data. |
| [List Elo](actions/get-elo.md) | GET | Retrieves historical Elo ratings from College Football Data. |
| [List F B S Teams](actions/get-fbs-teams.md) | GET | Retrieves FBS teams from College Football Data. |
| [List F P I](actions/get-fpi.md) | GET | Retrieves historical FPI ratings from College Football Data. |
| [Get Matchup](actions/get-matchup.md) | GET | Retrieves historical team matchup details from College Football Data. |
| [List Predicted Points Added By Team](actions/get-predicted-points-added-by-team.md) | GET | Retrieves team PPA metrics by season from College Football Data. |
| [List Records](actions/get-records.md) | GET | Retrieves historical team records from College Football Data. |
| [List S P](actions/get-sp.md) | GET | Retrieves SP+ ratings from College Football Data. |
| [List S R S](actions/get-srs.md) | GET | Retrieves historical SRS ratings from College Football Data. |
| [List Talent](actions/get-talent.md) | GET | Retrieves team talent composite data from College Football Data. |
| [List Team Recruiting Rankings](actions/get-team-recruiting-rankings.md) | GET | Retrieves team recruiting rankings from College Football Data. |
| [List Team Stats](actions/get-team-stats.md) | GET | Retrieves team season statistics from College Football Data. |
| [List Teams](actions/get-teams.md) | GET | Retrieves team information from College Football Data. |
| [List Teams A T S](actions/get-teams-ats.md) | GET | Retrieves team ATS summaries from College Football Data. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Coaches](actions/get-coaches.md) | GET | Retrieves historical head coach records from College Football Data. |
| [Get User Info](actions/get-user-info.md) | GET | Retrieves user account details from College Football Data. |

