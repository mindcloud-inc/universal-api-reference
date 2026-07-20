# <img src="https://images.mindcloud.co/apps/icons/mlb-square-icon_1776455797237.png" alt="Major League Baseball logo" width="28" height="28"> Major League Baseball: Universal API

Access Major League Baseball schedule, game, team, player, standings, stats, draft, and reference data from the public MLB Stats API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/majorLeagueBaseball/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 130
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.mlb.com
- **Vendor API docs:** https://developer.stats.com/docs/read/baseball/mlb

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get attendance](actions/attendance-attendance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/majorLeagueBaseball/latest/actions/attendance-attendance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (130)

### Award

| Action | Method | Description |
| --- | --- | --- |
| [View awards info](actions/awards-awards.md) | GET |  |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [Get attendance](actions/attendance-attendance.md) | GET |  |
| [View recipients of an award](actions/awards-award-recipients.md) | GET |  |
| [Get Broadcasts](actions/broadcast-get-broadcasts.md) | GET |  |
| [View conference info](actions/conference-conferences.md) | GET |  |
| [Reference List all stat fields](actions/config-aggregate-sort-enum.md) | GET |  |
| [List all awards](actions/config-awards.md) | GET |  |
| [List all baseball stats](actions/config-baseball-stats.md) | GET |  |
| [Reference List all event types](actions/config-event-types.md) | GET |  |
| [List fielder detail types](actions/config-fielder-detail-types.md) | GET |  |
| [List all status types](actions/config-game-status.md) | GET |  |
| [List all game types](actions/config-game-types.md) | GET |  |
| [Reference List all hit trajectories](actions/config-gameday-types.md) | GET |  |
| [Reference List groupBy types](actions/config-group-by-types.md) | GET |  |
| [Reference List all hit trajectories](actions/config-hit-trajectories.md) | GET |  |
| [List all job types](actions/config-job-types.md) | GET |  |
| [List all support languages](actions/config-languages.md) | GET |  |
| [List all possible player league leader types](actions/config-league-leader-types.md) | GET |  |
| [List all logical event types](actions/config-logical-events.md) | GET |  |
| [List all possible metrics](actions/config-metrics.md) | GET |  |
| [List all pitch codes](actions/config-pitch-codes.md) | GET |  |
| [List all pitch classification types](actions/config-pitch-types.md) | GET |  |
| [List all possible platforms](actions/config-platforms.md) | GET |  |
| [List all player status codes](actions/config-player-status-codes.md) | GET |  |
| [List all possible positions](actions/config-positions.md) | GET |  |
| [List all replay review reasons](actions/config-review-reasons.md) | GET |  |
| [List all possible roster types](actions/config-roster-types.md) | GET |  |
| [List runner detail types](actions/config-runner-detail-types.md) | GET |  |
| [Reference List all event types](actions/config-schedule-event-types.md) | GET |  |
| [List all situation codes](actions/config-sit-codes.md) | GET |  |
| [List all sky options](actions/config-sky.md) | GET |  |
| [List all standings types](actions/config-standings-types.md) | GET |  |
| [Reference List all stat fields](actions/config-stat-fields.md) | GET |  |
| [List all stat groups](actions/config-stat-groups.md) | GET |  |
| [Stats Search Config Endpoint](actions/config-stat-search-config.md) | GET |  |
| [Reference List groupBy types](actions/config-stat-search-group-by-types.md) | GET |  |
| [List stat search parameters](actions/config-stat-search-params.md) | GET |  |
| [List stat search stats](actions/config-stat-search-stats.md) | GET |  |
| [List all stat types](actions/config-stat-types.md) | GET |  |
| [Reference List all hit trajectories](actions/config-transaction-types.md) | GET |  |
| [List all wind direction options](actions/config-wind-direction.md) | GET |  |
| [Get division information](actions/division-divisions.md) | GET |  |
| [View MLB Drafted Players](actions/draft-draft-picks.md) | GET |  |
| [View MLB Draft Prospects](actions/draft-draft-prospects.md) | GET |  |
| [Get the last drafted player and the next 5 teams up to pick](actions/draft-latest-draft-picks.md) | GET |  |
| [Get game boxscore](actions/game-boxscore.md) | GET |  |
| [Get game color diff patch](actions/game-color-diff-patch.md) | GET |  |
| [Get game color feed](actions/game-color-feed.md) | GET |  |
| [Retrieve all of the color timestamps for a game](actions/game-color-timestamps.md) | GET |  |
| [Retrieve all content for a game](actions/game-content.md) | GET |  |
| [View a game change log](actions/game-current-game-stats.md) | GET |  |
| [Get the context metrics for this game based on its current state](actions/game-get-game-context-metrics.md) | GET |  |
| [Get the win probability for this game](actions/game-get-win-probability.md) | GET |  |
| [Get game linescore](actions/game-linescore.md) | GET |  |
| [Game Get live game status](actions/game-live-game-diff-patch-v1.md) | GET |  |
| [Game Get live game status](actions/game-live-game-v1.md) | GET |  |
| [Retrieve all of the play timestamps for a game](actions/game-live-timestampv11.md) | GET |  |
| [Get game pace](actions/game-pace.md) | GET |  |
| [Get game play By Play](actions/game-play-by-play.md) | GET |  |
| [Get game uniforms](actions/game-uniforms.md) | GET |  |
| [View high/low stats by player or team](actions/highlow-high-low.md) | GET |  |
| [View high/low stat types](actions/highlow-high-low-stats.md) | GET |  |
| [Home Run Derby View a home run derby object](actions/homerunderby-home-run-derby.md) | GET |  |
| [Home Run Derby View a home run derby object](actions/homerunderby-home-run-derby-bracket.md) | GET |  |
| [Home Run Derby View a home run derby object](actions/homerunderby-home-run-derby-game-bracket.md) | GET |  |
| [Home Run Derby View a home run derby object](actions/homerunderby-home-run-derby-game-pool.md) | GET |  |
| [Home Run Derby View a home run derby object](actions/homerunderby-home-run-derby-pool.md) | GET |  |
| [Job Get jobs by type](actions/job-datacasters.md) | GET |  |
| [Job Get jobs by type](actions/job-get-jobs-by-type.md) | GET |  |
| [Job Get jobs by type](actions/job-official-scorers.md) | GET |  |
| [Get umpire games](actions/job-umpire-games.md) | GET |  |
| [Job Get jobs by type](actions/job-umpires.md) | GET |  |
| [View league all-star ballot](actions/league-all-star-ballot.md) | GET |  |
| [League View league info](actions/league-all-star-final-vote.md) | GET |  |
| [League View league info](actions/league-all-star-write-ins.md) | GET |  |
| [League View league info](actions/league-all-stars-final-vote.md) | GET |  |
| [League View league info](actions/league-all-stars-write-ins.md) | GET |  |
| [View league info](actions/league-league.md) | GET |  |
| [View meta values](actions/meta-meta.md) | GET |  |
| [View available achievementStatus options](actions/milestones-achievement-statuses.md) | GET |  |
| [View available milestoneDurations options](actions/milestones-milestone-durations.md) | GET |  |
| [Milestone View available milestoneType options](actions/milestones-milestone-lookups.md) | GET |  |
| [View available milestone statistics options](actions/milestones-milestone-statistics.md) | GET |  |
| [Milestone View available milestoneType options](actions/milestones-milestone-types.md) | GET |  |
| [View pending and achieved milestones](actions/milestones-milestones.md) | GET |  |
| [View a players awards](actions/person-award.md) | GET |  |
| [View a players change log](actions/person-changes.md) | GET |  |
| [Person View a players stats](actions/person-current-game-stats.md) | GET |  |
| [Free Agents](actions/person-free-agents.md) | GET |  |
| [Person View a players stats](actions/person-game-stats.md) | GET |  |
| [View person info](actions/person-get-person.md) | GET |  |
| [Person View a players stats](actions/person-person.md) | GET |  |
| [View postseason schedule](actions/schedule-postseason.md) | GET |  |
| [Schedule View schedule info](actions/schedule-postseason-schedule-series.md) | GET |  |
| [Schedule View schedule info](actions/schedule-schedule.md) | GET |  |
| [Schedule View schedule info](actions/schedule-schedule-type.md) | GET |  |
| [Schedule View schedule info](actions/schedule-tie-games.md) | GET |  |
| [Schedule View schedule info](actions/schedule-tune-in.md) | GET |  |
| [View all seasons](actions/season-all-seasons.md) | GET |  |
| [Season View season info](actions/season-season.md) | GET |  |
| [Season View season info](actions/season-seasons.md) | GET |  |
| [Get all players for a sport level](actions/sports-sport-players.md) | GET |  |
| [List sports](actions/sports-sports.md) | GET |  |
| [View standings](actions/standings-base.md) | GET |  |
| [View standings for a league](actions/standings-standings.md) | GET |  |
| [Stats View stats](actions/stats-grouped-stats.md) | GET |  |
| [Get leaders for a statistic](actions/stats-leaders.md) | GET |  |
| [Stats View stats](actions/stats-stats.md) | GET |  |
| [View stat streaks](actions/stats-streaks.md) | GET |  |
| [View streaks](actions/streaks-get-streaks.md) | GET |  |
| [View streaks parameter options](actions/streaks-high-low-stats.md) | GET |  |
| [Team View team and affiliate teams](actions/team-affiliates.md) | GET |  |
| [Team View historical records for a list of teams](actions/team-all-teams.md) | GET |  |
| [View all team alumni](actions/team-alumni.md) | GET |  |
| [View all coaches for a team](actions/team-coaches.md) | GET |  |
| [Team View historical records for a list of teams](actions/team-history.md) | GET |  |
| [View in](actions/team-leaders.md) | GET |  |
| [View team personnel](actions/team-personnel.md) | GET |  |
| [View a teams info](actions/team-roster.md) | GET |  |
| [View team roster](actions/team-roster-base.md) | GET |  |
| [View a teams stats](actions/team-stats.md) | GET |  |
| [View leaders for team stats](actions/team-stats-leaders.md) | GET |  |
| [View team info](actions/team-team.md) | GET |  |
| [Team View team and affiliate teams](actions/team-team-affiliates.md) | GET |  |
| [View team stats](actions/team-team-stats.md) | GET |  |
| [View info for all teams](actions/team-teams.md) | GET |  |
| [Get team uniforms](actions/team-uniforms.md) | GET |  |
| [Update Alumni](actions/team-update-alumni.md) | GET |  |
| [List transactions](actions/transactions-transactions.md) | GET |  |
| [View venues](actions/venue-venues.md) | GET |  |

