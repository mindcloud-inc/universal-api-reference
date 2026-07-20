# Major League Baseball: Native API Reference

A consolidated summary of Major League Baseball's API configuration and 130 documented operations, with links to official documentation.

- **Official docs:** https://developer.stats.com/docs/read/baseball/mlb
- **API base URL:** `https://statsapi.mlb.com/api`

## Authentication

### No Authentication

The public MLB Stats API does not require tenant credentials for read-only requests.

This API does not require request authentication.

[Official authentication documentation](https://developer.stats.com/docs/read/baseball/mlb)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (130 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get attendance](actions/attendance-attendance.md) | `GET /v1/attendance` | [docs](https://github.com/toddrob99/MLB-StatsAPI/wiki/Endpoints) |
| [View recipients of an award](actions/awards-award-recipients.md) | `GET /v1/awards/{awardId}/recipients` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [View awards info](actions/awards-awards.md) | `GET /v1/awards/{awardId}` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Get Broadcasts](actions/broadcast-get-broadcasts.md) | `GET /v1/broadcast` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [View conference info](actions/conference-conferences.md) | `GET /v1/conferences` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Reference List all stat fields](actions/config-aggregate-sort-enum.md) | `GET /v1/sortModifiers` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [List all awards](actions/config-awards.md) | `GET /v1/awards` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [List all baseball stats](actions/config-baseball-stats.md) | `GET /v1/baseballStats` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Reference List all event types](actions/config-event-types.md) | `GET /v1/eventTypes` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [List fielder detail types](actions/config-fielder-detail-types.md) | `GET /v1/fielderDetailTypes` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [List all status types](actions/config-game-status.md) | `GET /v1/gameStatus` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [List all game types](actions/config-game-types.md) | `GET /v1/gameTypes` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Reference List all hit trajectories](actions/config-gameday-types.md) | `GET /v1/gamedayTypes` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Reference List groupBy types](actions/config-group-by-types.md) | `GET /v1/groupByTypes` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Reference List all hit trajectories](actions/config-hit-trajectories.md) | `GET /v1/hitTrajectories` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [List all job types](actions/config-job-types.md) | `GET /v1/jobTypes` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [List all support languages](actions/config-languages.md) | `GET /v1/languages` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [List all possible player league leader types](actions/config-league-leader-types.md) | `GET /v1/leagueLeaderTypes` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [List all logical event types](actions/config-logical-events.md) | `GET /v1/logicalEvents` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [List all possible metrics](actions/config-metrics.md) | `GET /v1/metrics` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [List all pitch codes](actions/config-pitch-codes.md) | `GET /v1/pitchCodes` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [List all pitch classification types](actions/config-pitch-types.md) | `GET /v1/pitchTypes` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [List all possible platforms](actions/config-platforms.md) | `GET /v1/platforms` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [List all player status codes](actions/config-player-status-codes.md) | `GET /v1/playerStatusCodes` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [List all possible positions](actions/config-positions.md) | `GET /v1/positions` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [List all replay review reasons](actions/config-review-reasons.md) | `GET /v1/reviewReasons` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [List all possible roster types](actions/config-roster-types.md) | `GET /v1/rosterTypes` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [List runner detail types](actions/config-runner-detail-types.md) | `GET /v1/runnerDetailTypes` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Reference List all event types](actions/config-schedule-event-types.md) | `GET /v1/scheduleEventTypes` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [List all situation codes](actions/config-sit-codes.md) | `GET /v1/situationCodes` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [List all sky options](actions/config-sky.md) | `GET /v1/sky` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [List all standings types](actions/config-standings-types.md) | `GET /v1/standingsTypes` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Reference List all stat fields](actions/config-stat-fields.md) | `GET /v1/statFields` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [List all stat groups](actions/config-stat-groups.md) | `GET /v1/statGroups` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Stats Search Config Endpoint](actions/config-stat-search-config.md) | `GET /v1/stats/search/config` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Reference List groupBy types](actions/config-stat-search-group-by-types.md) | `GET /v1/stats/search/groupByTypes` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [List stat search parameters](actions/config-stat-search-params.md) | `GET /v1/stats/search/params` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [List stat search stats](actions/config-stat-search-stats.md) | `GET /v1/stats/search/stats` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [List all stat types](actions/config-stat-types.md) | `GET /v1/statTypes` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Reference List all hit trajectories](actions/config-transaction-types.md) | `GET /v1/transactionTypes` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [List all wind direction options](actions/config-wind-direction.md) | `GET /v1/windDirection` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Get division information](actions/division-divisions.md) | `GET /v1/divisions` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [View MLB Drafted Players](actions/draft-draft-picks.md) | `GET /v1/draft/{year}` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [View MLB Draft Prospects](actions/draft-draft-prospects.md) | `GET /v1/draft/prospects/{year}` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Get the last drafted player and the next 5 teams up to pick](actions/draft-latest-draft-picks.md) | `GET /v1/draft/{year}/latest` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Get game boxscore](actions/game-boxscore.md) | `GET /v1/game/{game_pk}/boxscore` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Get game color diff patch](actions/game-color-diff-patch.md) | `GET /v1/game/{gamePk}/feed/color/diffPatch` | [docs](https://github.com/toddrob99/MLB-StatsAPI/wiki/Endpoints) |
| [Get game color feed](actions/game-color-feed.md) | `GET /v1/game/{game_pk}/feed/color` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Retrieve all of the color timestamps for a game](actions/game-color-timestamps.md) | `GET /v1/game/{game_pk}/feed/color/timestamps` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Retrieve all content for a game](actions/game-content.md) | `GET /v1/game/{game_pk}/content` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [View a game change log](actions/game-current-game-stats.md) | `GET /v1/game/changes` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Get the context metrics for this game based on its current state](actions/game-get-game-context-metrics.md) | `GET /v1/game/{gamePk}/contextMetrics` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Get the win probability for this game](actions/game-get-win-probability.md) | `GET /v1/game/{gamePk}/winProbability` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Get game linescore](actions/game-linescore.md) | `GET /v1/game/{game_pk}/linescore` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Game Get live game status](actions/game-live-game-diff-patch-v1.md) | `GET /v1.1/game/{game_pk}/feed/live/diffPatch` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Game Get live game status](actions/game-live-game-v1.md) | `GET /v1.1/game/{game_pk}/feed/live` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Retrieve all of the play timestamps for a game](actions/game-live-timestampv11.md) | `GET /v1.1/game/{game_pk}/feed/live/timestamps` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Get game pace](actions/game-pace.md) | `GET /v1/gamePace` | [docs](https://github.com/toddrob99/MLB-StatsAPI/wiki/Endpoints) |
| [Get game play By Play](actions/game-play-by-play.md) | `GET /v1/game/{game_pk}/playByPlay` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Get game uniforms](actions/game-uniforms.md) | `GET /v1/uniforms/game` | [docs](https://github.com/toddrob99/MLB-StatsAPI/wiki/Endpoints) |
| [View high/low stats by player or team](actions/highlow-high-low.md) | `GET /v1/highLow/types` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [View high/low stat types](actions/highlow-high-low-stats.md) | `GET /v1/highLow/{highLowType}` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Home Run Derby View a home run derby object](actions/homerunderby-home-run-derby.md) | `GET /v1/homeRunDerby` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Home Run Derby View a home run derby object](actions/homerunderby-home-run-derby-bracket.md) | `GET /v1/homeRunDerby/bracket` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Home Run Derby View a home run derby object](actions/homerunderby-home-run-derby-game-bracket.md) | `GET /v1/homeRunDerby/{gamePk}/bracket` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Home Run Derby View a home run derby object](actions/homerunderby-home-run-derby-game-pool.md) | `GET /v1/homeRunDerby/{gamePk}/pool` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Home Run Derby View a home run derby object](actions/homerunderby-home-run-derby-pool.md) | `GET /v1/homeRunDerby/pool` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Job Get jobs by type](actions/job-datacasters.md) | `GET /v1/jobs/datacasters` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Job Get jobs by type](actions/job-get-jobs-by-type.md) | `GET /v1/jobs` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Job Get jobs by type](actions/job-official-scorers.md) | `GET /v1/jobs/officialScorers` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Get umpire games](actions/job-umpire-games.md) | `GET /v1/jobs/umpires/games/{umpireId}` | [docs](https://github.com/toddrob99/MLB-StatsAPI/wiki/Endpoints) |
| [Job Get jobs by type](actions/job-umpires.md) | `GET /v1/jobs/umpires` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [View league all-star ballot](actions/league-all-star-ballot.md) | `GET /v1/league/{leagueId}/allStarBallot` | [docs](https://github.com/toddrob99/MLB-StatsAPI/wiki/Endpoints) |
| [League View league info](actions/league-all-star-final-vote.md) | `GET /v1/league/{leagueId}/allStarFinalVote` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [League View league info](actions/league-all-star-write-ins.md) | `GET /v1/league/{leagueId}/allStarWriteIns` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [League View league info](actions/league-all-stars-final-vote.md) | `GET /v1/leagues/{leagueId}/allStarFinalVote` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [League View league info](actions/league-all-stars-write-ins.md) | `GET /v1/leagues/{leagueId}/allStarWriteIns` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [View league info](actions/league-league.md) | `GET /v1/league` | [docs](https://github.com/toddrob99/MLB-StatsAPI/wiki/Endpoints) |
| [View meta values](actions/meta-meta.md) | `GET /v1/{type}` | [docs](https://github.com/toddrob99/MLB-StatsAPI/wiki/Endpoints) |
| [View available achievementStatus options](actions/milestones-achievement-statuses.md) | `GET /v1/achievementStatuses` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [View available milestoneDurations options](actions/milestones-milestone-durations.md) | `GET /v1/milestoneDurations` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Milestone View available milestoneType options](actions/milestones-milestone-lookups.md) | `GET /v1/milestoneLookups` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [View available milestone statistics options](actions/milestones-milestone-statistics.md) | `GET /v1/milestoneStatistics` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Milestone View available milestoneType options](actions/milestones-milestone-types.md) | `GET /v1/milestoneTypes` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [View pending and achieved milestones](actions/milestones-milestones.md) | `GET /v1/milestones` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [View a players awards](actions/person-award.md) | `GET /v1/people/{personId}/awards` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [View a players change log](actions/person-changes.md) | `GET /v1/people/changes` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Person View a players stats](actions/person-current-game-stats.md) | `GET /v1/people/{personId}/stats/game/current` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Free Agents](actions/person-free-agents.md) | `GET /v1/people/freeAgents` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Person View a players stats](actions/person-game-stats.md) | `GET /v1/people/{personId}/stats/game/{gamePk}` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [View person info](actions/person-get-person.md) | `GET /v1/people/{personId}` | [docs](https://github.com/toddrob99/MLB-StatsAPI/wiki/Endpoints) |
| [Person View a players stats](actions/person-person.md) | `GET /v1/people` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [View postseason schedule](actions/schedule-postseason.md) | `GET /v1/schedule/postseason` | [docs](https://github.com/toddrob99/MLB-StatsAPI/wiki/Endpoints) |
| [Schedule View schedule info](actions/schedule-postseason-schedule-series.md) | `GET /v1/schedule/postseason/series` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Schedule View schedule info](actions/schedule-schedule.md) | `GET /v1/schedule` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Schedule View schedule info](actions/schedule-schedule-type.md) | `GET /v1/schedule/{scheduleType}` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Schedule View schedule info](actions/schedule-tie-games.md) | `GET /v1/schedule/games/tied` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Schedule View schedule info](actions/schedule-tune-in.md) | `GET /v1/schedule/postseason/tuneIn` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [View all seasons](actions/season-all-seasons.md) | `GET /v1/seasons/all` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Season View season info](actions/season-season.md) | `GET /v1/seasons/{seasonId}` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Season View season info](actions/season-seasons.md) | `GET /v1/seasons` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Get all players for a sport level](actions/sports-sport-players.md) | `GET /v1/sports/{sportId}/players` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [List sports](actions/sports-sports.md) | `GET /v1/sports` | [docs](https://github.com/toddrob99/MLB-StatsAPI/wiki/Endpoints) |
| [View standings](actions/standings-base.md) | `GET /v1/standings` | [docs](https://github.com/toddrob99/MLB-StatsAPI/wiki/Endpoints) |
| [View standings for a league](actions/standings-standings.md) | `GET /v1/standings/{standingsType}` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Stats View stats](actions/stats-grouped-stats.md) | `GET /v1/stats/grouped` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Get leaders for a statistic](actions/stats-leaders.md) | `GET /v1/stats/leaders` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Stats View stats](actions/stats-stats.md) | `GET /v1/stats` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [View stat streaks](actions/stats-streaks.md) | `GET /v1/stats/streaks` | [docs](https://github.com/toddrob99/MLB-StatsAPI/wiki/Endpoints) |
| [View streaks](actions/streaks-get-streaks.md) | `GET /v1/streaks` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [View streaks parameter options](actions/streaks-high-low-stats.md) | `GET /v1/streaks/types` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Team View team and affiliate teams](actions/team-affiliates.md) | `GET /v1/teams/affiliates` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Team View historical records for a list of teams](actions/team-all-teams.md) | `GET /v1/teams/history` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [View all team alumni](actions/team-alumni.md) | `GET /v1/teams/{teamId}/alumni` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [View all coaches for a team](actions/team-coaches.md) | `GET /v1/teams/{teamId}/coaches` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Team View historical records for a list of teams](actions/team-history.md) | `GET /v1/teams/{teamId}/history` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [View in](actions/team-leaders.md) | `GET /v1/teams/{teamId}/leaders` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [View team personnel](actions/team-personnel.md) | `GET /v1/teams/{teamId}/personnel` | [docs](https://github.com/toddrob99/MLB-StatsAPI/wiki/Endpoints) |
| [View a teams info](actions/team-roster.md) | `GET /v1/teams/{teamId}/roster/{rosterType}` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [View team roster](actions/team-roster-base.md) | `GET /v1/teams/{teamId}/roster` | [docs](https://github.com/toddrob99/MLB-StatsAPI/wiki/Endpoints) |
| [View a teams stats](actions/team-stats.md) | `GET /v1/teams/stats` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [View leaders for team stats](actions/team-stats-leaders.md) | `GET /v1/teams/stats/leaders` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [View team info](actions/team-team.md) | `GET /v1/teams/{teamId}` | [docs](https://github.com/toddrob99/MLB-StatsAPI/wiki/Endpoints) |
| [Team View team and affiliate teams](actions/team-team-affiliates.md) | `GET /v1/teams/{teamId}/affiliates` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [View team stats](actions/team-team-stats.md) | `GET /v1/teams/{teamId}/stats` | [docs](https://github.com/toddrob99/MLB-StatsAPI/wiki/Endpoints) |
| [View info for all teams](actions/team-teams.md) | `GET /v1/teams` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [Get team uniforms](actions/team-uniforms.md) | `GET /v1/uniforms/team` | [docs](https://github.com/toddrob99/MLB-StatsAPI/wiki/Endpoints) |
| [Update Alumni](actions/team-update-alumni.md) | `GET /v1/teams/{teamId}/alumni` | [docs](https://developer.stats.com/docs/read/baseball/mlb) |
| [List transactions](actions/transactions-transactions.md) | `GET /v1/transactions` | [docs](https://github.com/toddrob99/MLB-StatsAPI/wiki/Endpoints) |
| [View venues](actions/venue-venues.md) | `GET /v1/venues` | [docs](https://github.com/toddrob99/MLB-StatsAPI/wiki/Endpoints) |
