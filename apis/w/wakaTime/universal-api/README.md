# <img src="https://images.mindcloud.co/apps/icons/wakatime-icon_1776351940455.png" alt="WakaTime logo" width="28" height="28"> WakaTime: Universal API

Access WakaTime coding activity, stats, summaries, heartbeats, goals, leaderboards, organizations, and related analytics through the official WakaTime API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/wakaTime/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 87
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://wakatime.com
- **Vendor API docs:** https://wakatime.com/developers

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wakaTime/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (87)

### Aggregated Stat

| Action | Method | Description |
| --- | --- | --- |
| [Get Aggregated Stats Range](actions/get-aggregated-stats-range.md) | GET | Retrieves aggregated coding stats for a WakaTime time range. |

### All Time Since Today

| Action | Method | Description |
| --- | --- | --- |
| [Get All Time Since Today](actions/get-all-time-since-today.md) | GET | Retrieves total logged time since account creation from WakaTime. |
| [Get Current All Time Since Today](actions/get-current-all-time-since-today.md) | GET | Retrieves total logged time since account creation from WakaTime. |

### Commit

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Project Commit](actions/get-current-project-commit.md) | GET | Retrieves a commit from a WakaTime project. |
| [Get Project Commit](actions/get-project-commit.md) | GET | Retrieves a commit from a WakaTime project. |
| [List Current Project Commits](actions/list-current-project-commits.md) | GET | Retrieves commits from a WakaTime project. |
| [List Project Commits](actions/list-project-commits.md) | GET | Retrieves commits from a WakaTime project. |

### Custom Rule

| Action | Method | Description |
| --- | --- | --- |
| [Delete Current Custom Rule](actions/delete-current-custom-rule.md) | DELETE | Deletes a custom rule from WakaTime. |
| [Delete Custom Rule](actions/delete-custom-rule.md) | DELETE | Deletes a custom rule from WakaTime. |
| [List Current Custom Rules](actions/list-current-custom-rules.md) | GET | Retrieves custom rules from WakaTime. |
| [List Custom Rules](actions/list-custom-rules.md) | GET | Retrieves custom rules from WakaTime. |
| [Upsert Current Custom Rule](actions/upsert-current-custom-rule.md) | PUT | Updates custom rules in WakaTime. |
| [Upsert Custom Rule](actions/upsert-custom-rule.md) | PUT | Updates custom rules in WakaTime. |

### Custom Rules Progress

| Action | Method | Description |
| --- | --- | --- |
| [Delete Current Custom Rules Progress](actions/delete-current-custom-rules-progress.md) | DELETE | Aborts applying custom rules in WakaTime. |
| [Delete Custom Rules Progress](actions/delete-custom-rules-progress.md) | DELETE | Aborts applying custom rules in WakaTime. |
| [Get Current Custom Rules Progress](actions/get-current-custom-rules-progress.md) | GET | Retrieves custom rule application progress from WakaTime. |
| [Get Custom Rules Progress](actions/get-custom-rules-progress.md) | GET | Retrieves custom rule application progress from WakaTime. |

### Dashboard

| Action | Method | Description |
| --- | --- | --- |
| [List Current Org Dashboards](actions/list-current-org-dashboards.md) | GET | Retrieves dashboards for a WakaTime organization. |
| [List Org Dashboards](actions/list-org-dashboards.md) | GET | Retrieves dashboards for a WakaTime organization. |

### Dashboard Duration

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Org Dashboard Durations](actions/get-current-org-dashboard-durations.md) | GET | Retrieves daily durations for a WakaTime organization dashboard. |
| [Get Org Dashboard Durations](actions/get-org-dashboard-durations.md) | GET | Retrieves daily durations for a WakaTime organization dashboard. |

### Dashboard Member

| Action | Method | Description |
| --- | --- | --- |
| [List Current Org Dashboard Members](actions/list-current-org-dashboard-members.md) | GET | Retrieves members of a WakaTime organization dashboard. |
| [List Org Dashboard Members](actions/list-org-dashboard-members.md) | GET | Retrieves members of a WakaTime organization dashboard. |

### Dashboard Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Org Dashboard Summaries](actions/get-current-org-dashboard-summaries.md) | GET | Retrieves daily summaries for a WakaTime organization dashboard. |
| [Get Org Dashboard Summaries](actions/get-org-dashboard-summaries.md) | GET | Retrieves daily summaries for a WakaTime organization dashboard. |

### Data Dump

| Action | Method | Description |
| --- | --- | --- |
| [Create Current Data Dump](actions/create-current-data-dump.md) | POST | Creates a WakaTime data export. |
| [Create Data Dump](actions/create-data-dump.md) | POST | Creates a WakaTime data export. |
| [List Current Data Dumps](actions/list-current-data-dumps.md) | GET | Retrieves a user's WakaTime data exports. |
| [List Data Dumps](actions/list-data-dumps.md) | GET | Retrieves a user's WakaTime data exports. |

### Duration

| Action | Method | Description |
| --- | --- | --- |
| [List Current Durations](actions/list-current-durations.md) | GET | Retrieves daily coding durations from WakaTime. |
| [List Durations](actions/list-durations.md) | GET | Retrieves daily coding durations from WakaTime. |

### Editor

| Action | Method | Description |
| --- | --- | --- |
| [List Editors](actions/list-editors.md) | GET | Retrieves WakaTime editor plugins. |

### External Duration

| Action | Method | Description |
| --- | --- | --- |
| [Create Current External Duration](actions/create-current-external-duration.md) | POST | Creates or updates an external duration in WakaTime by external ID. |
| [Create Current External Durations Bulk](actions/create-current-external-durations-bulk.md) | POST | Creates or updates external durations in WakaTime by external ID. |
| [Create External Duration](actions/create-external-duration.md) | POST | Creates or updates an external duration in WakaTime by external ID. |
| [Create External Durations Bulk](actions/create-external-durations-bulk.md) | POST | Creates or updates external durations in WakaTime by external ID. |
| [Delete Current External Durations Bulk](actions/delete-current-external-durations-bulk.md) | DELETE | Deletes multiple external durations from WakaTime. |
| [Delete External Durations Bulk](actions/delete-external-durations-bulk.md) | DELETE | Deletes multiple external durations from WakaTime. |
| [List Current External Durations](actions/list-current-external-durations.md) | GET | Retrieves daily external durations from WakaTime. |
| [List External Durations](actions/list-external-durations.md) | GET | Retrieves daily external durations from WakaTime. |

### Goal

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Goal](actions/get-current-goal.md) | GET | Retrieves a specific coding goal from WakaTime. |
| [Get Goal](actions/get-goal.md) | GET | Retrieves a specific coding goal from WakaTime. |
| [List Current Goals](actions/list-current-goals.md) | GET | Retrieves coding goals from WakaTime. |
| [List Goals](actions/list-goals.md) | GET | Retrieves coding goals from WakaTime. |

### Heartbeat

| Action | Method | Description |
| --- | --- | --- |
| [Create Current Heartbeat](actions/create-current-heartbeat.md) | POST | Creates a heartbeat in WakaTime. |
| [Create Current Heartbeats Bulk](actions/create-current-heartbeats-bulk.md) | POST | Creates multiple heartbeats in WakaTime. |
| [Create Heartbeat](actions/create-heartbeat.md) | POST | Creates a heartbeat in WakaTime. |
| [Create Heartbeats Bulk](actions/create-heartbeats-bulk.md) | POST | Creates multiple heartbeats in WakaTime. |
| [Delete Current Heartbeats Bulk](actions/delete-current-heartbeats-bulk.md) | DELETE | Deletes multiple heartbeats from WakaTime. |
| [Delete Heartbeats Bulk](actions/delete-heartbeats-bulk.md) | DELETE | Deletes multiple heartbeats from WakaTime. |
| [List Current Heartbeats](actions/list-current-heartbeats.md) | GET | Retrieves daily heartbeats from WakaTime. |
| [List Heartbeats](actions/list-heartbeats.md) | GET | Retrieves daily heartbeats from WakaTime. |

### Insight

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Insights](actions/get-current-insights.md) | GET | Retrieves a coding activity insight from WakaTime. |
| [Get Insights](actions/get-insights.md) | GET | Retrieves a coding activity insight from WakaTime. |

### Leader

| Action | Method | Description |
| --- | --- | --- |
| [List Public Leaders](actions/list-public-leaders.md) | GET | Retrieves ranked users from WakaTime's public leaderboard. |

### Machine Name

| Action | Method | Description |
| --- | --- | --- |
| [List Current Machine Names](actions/list-current-machine-names.md) | GET | Retrieves a user's WakaTime machines. |
| [List Machine Names](actions/list-machine-names.md) | GET | Retrieves a user's WakaTime machines. |

### Member Duration

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Org Dashboard Member Durations](actions/get-current-org-dashboard-member-durations.md) | GET | Retrieves daily durations for a WakaTime dashboard member. |
| [Get Org Dashboard Member Durations](actions/get-org-dashboard-member-durations.md) | GET | Retrieves daily durations for a WakaTime dashboard member. |

### Member Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Org Dashboard Member Summaries](actions/get-current-org-dashboard-member-summaries.md) | GET | Retrieves daily summaries for a WakaTime dashboard member. |
| [Get Org Dashboard Member Summaries](actions/get-org-dashboard-member-summaries.md) | GET | Retrieves daily summaries for a WakaTime dashboard member. |

### Meta

| Action | Method | Description |
| --- | --- | --- |
| [Get Meta](actions/get-meta.md) | GET | Retrieves WakaTime metadata and public server IPs. |

### Org Custom Rule

| Action | Method | Description |
| --- | --- | --- |
| [List Current Org Custom Rules](actions/list-current-org-custom-rules.md) | GET | Retrieves custom rules for a WakaTime organization. |
| [List Org Custom Rules](actions/list-org-custom-rules.md) | GET | Retrieves custom rules for a WakaTime organization. |
| [Upsert Current Org Custom Rule](actions/upsert-current-org-custom-rule.md) | PUT | Updates custom rules for a WakaTime organization. |
| [Upsert Org Custom Rule](actions/upsert-org-custom-rule.md) | PUT | Updates custom rules for a WakaTime organization. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [List Current Orgs](actions/list-current-orgs.md) | GET | Retrieves a user's WakaTime organizations. |
| [List Orgs](actions/list-orgs.md) | GET | Retrieves a user's WakaTime organizations. |

### Private Leaderboard

| Action | Method | Description |
| --- | --- | --- |
| [List Current Private Leaderboards](actions/list-current-private-leaderboards.md) | GET | Retrieves private leaderboards from WakaTime. |
| [List Private Leaderboards](actions/list-private-leaderboards.md) | GET | Retrieves private leaderboards from WakaTime. |

### Private Leaderboard Leader

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Private Leaderboard Leaders](actions/get-current-private-leaderboard-leaders.md) | GET | Retrieves ranked users from a private WakaTime leaderboard. |
| [Get Private Leaderboard Leaders](actions/get-private-leaderboard-leaders.md) | GET | Retrieves ranked users from a private WakaTime leaderboard. |

### Program Language

| Action | Method | Description |
| --- | --- | --- |
| [List Program Languages](actions/list-program-languages.md) | GET | Retrieves verified programming languages from WakaTime. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [List Current Projects](actions/list-current-projects.md) | GET | Retrieves WakaTime projects for a user. |
| [List Projects](actions/list-projects.md) | GET | Retrieves WakaTime projects for a user. |

### Stat

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Stats Range](actions/get-current-stats-range.md) | GET | Retrieves coding stats for a WakaTime time range. |
| [Get Stats Range](actions/get-stats-range.md) | GET | Retrieves coding stats for a WakaTime time range. |
| [List Current Stats](actions/list-current-stats.md) | GET | Retrieves coding stats from WakaTime. |
| [List Stats](actions/list-stats.md) | GET | Retrieves coding stats from WakaTime. |

### Status Bar

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Status Bar Today](actions/get-current-status-bar-today.md) | GET | Retrieves today's status bar summary from WakaTime. |
| [Get Status Bar Today](actions/get-status-bar-today.md) | GET | Retrieves today's status bar summary from WakaTime. |

### Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Summaries](actions/get-current-summaries.md) | GET | Retrieves daily coding summaries from WakaTime. |
| [Get Summaries](actions/get-summaries.md) | GET | Retrieves daily coding summaries from WakaTime. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current WakaTime user. |
| [Get User Profile](actions/get-user-profile.md) | GET | Retrieves a WakaTime user's profile. |

### User Agent

| Action | Method | Description |
| --- | --- | --- |
| [List Current User Agents](actions/list-current-user-agents.md) | GET | Retrieves a user's WakaTime plugin user agents. |
| [List User Agents](actions/list-user-agents.md) | GET | Retrieves a user's WakaTime plugin user agents. |

