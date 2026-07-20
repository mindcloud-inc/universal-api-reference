# WakaTime: Native API Reference

A consolidated summary of WakaTime's API configuration and 87 documented operations, with links to official documentation.

- **Official docs:** https://wakatime.com/developers
- **API base URL:** `https://api.wakatime.com/api/v1`

## Authentication

### OAuth2

Standard OAuth2 authorization-code flow for WakaTime user accounts.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://wakatime.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://wakatime.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `email read_goals read_heartbeats read_orgs read_private_leaderboards read_stats read_summaries write_heartbeats write_orgs write_private_leaderboards`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://wakatime.com/oauth/token.

[Official authentication documentation](https://wakatime.com/developers)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (87 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Current Data Dump](actions/create-current-data-dump.md) | `POST /users/current/data_dumps` | [docs](https://wakatime.com/developers#data_dumps) |
| [Create Current External Duration](actions/create-current-external-duration.md) | `POST /users/current/external_durations` | [docs](https://wakatime.com/developers#external_durations) |
| [Create Current External Durations Bulk](actions/create-current-external-durations-bulk.md) | `POST /users/current/external_durations.bulk` | [docs](https://wakatime.com/developers#external_durations) |
| [Create Current Heartbeat](actions/create-current-heartbeat.md) | `POST /users/current/heartbeats` | [docs](https://wakatime.com/developers#heartbeats) |
| [Create Current Heartbeats Bulk](actions/create-current-heartbeats-bulk.md) | `POST /users/current/heartbeats.bulk` | [docs](https://wakatime.com/developers#heartbeats) |
| [Create Data Dump](actions/create-data-dump.md) | `POST /users/:user/data_dumps` | [docs](https://wakatime.com/developers#data_dumps) |
| [Create External Duration](actions/create-external-duration.md) | `POST /users/:user/external_durations` | [docs](https://wakatime.com/developers#external_durations) |
| [Create External Durations Bulk](actions/create-external-durations-bulk.md) | `POST /users/:user/external_durations.bulk` | [docs](https://wakatime.com/developers#external_durations) |
| [Create Heartbeat](actions/create-heartbeat.md) | `POST /users/:user/heartbeats` | [docs](https://wakatime.com/developers#heartbeats) |
| [Create Heartbeats Bulk](actions/create-heartbeats-bulk.md) | `POST /users/:user/heartbeats.bulk` | [docs](https://wakatime.com/developers#heartbeats) |
| [Delete Current Custom Rule](actions/delete-current-custom-rule.md) | `DELETE /users/current/custom_rules/:rule_id` | [docs](https://wakatime.com/developers#custom_rules) |
| [Delete Current Custom Rules Progress](actions/delete-current-custom-rules-progress.md) | `DELETE /users/current/custom_rules_progress` | [docs](https://wakatime.com/developers#custom_rules_progress) |
| [Delete Current External Durations Bulk](actions/delete-current-external-durations-bulk.md) | `DELETE /users/current/external_durations.bulk` | [docs](https://wakatime.com/developers#external_durations) |
| [Delete Current Heartbeats Bulk](actions/delete-current-heartbeats-bulk.md) | `DELETE /users/current/heartbeats.bulk` | [docs](https://wakatime.com/developers#heartbeats) |
| [Delete Custom Rule](actions/delete-custom-rule.md) | `DELETE /users/:user/custom_rules/:rule_id` | [docs](https://wakatime.com/developers#custom_rules) |
| [Delete Custom Rules Progress](actions/delete-custom-rules-progress.md) | `DELETE /users/:user/custom_rules_progress` | [docs](https://wakatime.com/developers#custom_rules_progress) |
| [Delete External Durations Bulk](actions/delete-external-durations-bulk.md) | `DELETE /users/:user/external_durations.bulk` | [docs](https://wakatime.com/developers#external_durations) |
| [Delete Heartbeats Bulk](actions/delete-heartbeats-bulk.md) | `DELETE /users/:user/heartbeats.bulk` | [docs](https://wakatime.com/developers#heartbeats) |
| [Get Aggregated Stats Range](actions/get-aggregated-stats-range.md) | `GET /stats/:range` | [docs](https://wakatime.com/developers#stats_aggregated) |
| [Get All Time Since Today](actions/get-all-time-since-today.md) | `GET /users/:user/all_time_since_today` | [docs](https://wakatime.com/developers#all_time_since_today) |
| [Get Current All Time Since Today](actions/get-current-all-time-since-today.md) | `GET /users/current/all_time_since_today` | [docs](https://wakatime.com/developers#all_time_since_today) |
| [Get Current Custom Rules Progress](actions/get-current-custom-rules-progress.md) | `GET /users/current/custom_rules_progress` | [docs](https://wakatime.com/developers#custom_rules_progress) |
| [Get Current Goal](actions/get-current-goal.md) | `GET /users/current/goals/:goal` | [docs](https://wakatime.com/developers#goal) |
| [Get Current Insights](actions/get-current-insights.md) | `GET /users/current/insights/:insight_type/:range` | [docs](https://wakatime.com/developers#insights) |
| [Get Current Org Dashboard Durations](actions/get-current-org-dashboard-durations.md) | `GET /users/current/orgs/:orgs/dashboards/:dashboard/durations` | [docs](https://wakatime.com/developers#org_dashboard_durations) |
| [Get Current Org Dashboard Member Durations](actions/get-current-org-dashboard-member-durations.md) | `GET /users/current/orgs/:orgs/dashboards/:dashboard/members/:member/durations` | [docs](https://wakatime.com/developers#org_dashboard_member_durations) |
| [Get Current Org Dashboard Member Summaries](actions/get-current-org-dashboard-member-summaries.md) | `GET /users/current/orgs/:org/dashboards/:dashboard/members/:member/summaries` | [docs](https://wakatime.com/developers#org_dashboard_member_summaries) |
| [Get Current Org Dashboard Summaries](actions/get-current-org-dashboard-summaries.md) | `GET /users/current/orgs/:org/dashboards/:dashboard/summaries` | [docs](https://wakatime.com/developers#org_dashboard_summaries) |
| [Get Current Private Leaderboard Leaders](actions/get-current-private-leaderboard-leaders.md) | `GET /users/current/leaderboards/:board` | [docs](https://wakatime.com/developers#private_leaderboards_leaders) |
| [Get Current Project Commit](actions/get-current-project-commit.md) | `GET /users/current/projects/:project/commits/:hash` | [docs](https://wakatime.com/developers#commit) |
| [Get Current Stats Range](actions/get-current-stats-range.md) | `GET /users/current/stats/:range` | [docs](https://wakatime.com/developers#stats) |
| [Get Current Status Bar Today](actions/get-current-status-bar-today.md) | `GET /users/current/status_bar/today` | [docs](https://wakatime.com/developers#status_bar) |
| [Get Current Summaries](actions/get-current-summaries.md) | `GET /users/current/summaries` | [docs](https://wakatime.com/developers#summaries) |
| [Get Current User](actions/get-current-user.md) | `GET /users/current` | [docs](https://wakatime.com/developers#users) |
| [Get Custom Rules Progress](actions/get-custom-rules-progress.md) | `GET /users/:user/custom_rules_progress` | [docs](https://wakatime.com/developers#custom_rules_progress) |
| [Get Goal](actions/get-goal.md) | `GET /users/:user/goals/:goal` | [docs](https://wakatime.com/developers#goal) |
| [Get Insights](actions/get-insights.md) | `GET /users/:user/insights/:insight_type/:range` | [docs](https://wakatime.com/developers#insights) |
| [Get Meta](actions/get-meta.md) | `GET /meta` | [docs](https://wakatime.com/developers#meta) |
| [Get Org Dashboard Durations](actions/get-org-dashboard-durations.md) | `GET /users/:user/orgs/:org/dashboards/:dashboard/durations` | [docs](https://wakatime.com/developers#org_dashboard_durations) |
| [Get Org Dashboard Member Durations](actions/get-org-dashboard-member-durations.md) | `GET /users/:user/orgs/:org/dashboards/:dashboard/members/:member/durations` | [docs](https://wakatime.com/developers#org_dashboard_member_durations) |
| [Get Org Dashboard Member Summaries](actions/get-org-dashboard-member-summaries.md) | `GET /users/:user/orgs/:org/dashboards/:dashboard/members/:member/summaries` | [docs](https://wakatime.com/developers#org_dashboard_member_summaries) |
| [Get Org Dashboard Summaries](actions/get-org-dashboard-summaries.md) | `GET /users/:user/orgs/:org/dashboards/:dashboard/summaries` | [docs](https://wakatime.com/developers#org_dashboard_summaries) |
| [Get Private Leaderboard Leaders](actions/get-private-leaderboard-leaders.md) | `GET /users/:user/leaderboards/:board` | [docs](https://wakatime.com/developers#private_leaderboards_leaders) |
| [Get Project Commit](actions/get-project-commit.md) | `GET /users/:user/projects/:project/commits/:hash` | [docs](https://wakatime.com/developers#commit) |
| [Get Stats Range](actions/get-stats-range.md) | `GET /users/:user/stats/:range` | [docs](https://wakatime.com/developers#stats) |
| [Get Status Bar Today](actions/get-status-bar-today.md) | `GET /users/:user/status_bar/today` | [docs](https://wakatime.com/developers#status_bar) |
| [Get Summaries](actions/get-summaries.md) | `GET /users/:user/summaries` | [docs](https://wakatime.com/developers#summaries) |
| [Get User Profile](actions/get-user-profile.md) | `GET /users/:user` | [docs](https://wakatime.com/developers#users) |
| [List Current Custom Rules](actions/list-current-custom-rules.md) | `GET /users/current/custom_rules` | [docs](https://wakatime.com/developers#custom_rules) |
| [List Current Data Dumps](actions/list-current-data-dumps.md) | `GET /users/current/data_dumps` | [docs](https://wakatime.com/developers#data_dumps) |
| [List Current Durations](actions/list-current-durations.md) | `GET /users/current/durations` | [docs](https://wakatime.com/developers#durations) |
| [List Current External Durations](actions/list-current-external-durations.md) | `GET /users/current/external_durations` | [docs](https://wakatime.com/developers#external_durations) |
| [List Current Goals](actions/list-current-goals.md) | `GET /users/current/goals` | [docs](https://wakatime.com/developers#goals) |
| [List Current Heartbeats](actions/list-current-heartbeats.md) | `GET /users/current/heartbeats` | [docs](https://wakatime.com/developers#heartbeats) |
| [List Current Machine Names](actions/list-current-machine-names.md) | `GET /users/current/machine_names` | [docs](https://wakatime.com/developers#machine_names) |
| [List Current Org Custom Rules](actions/list-current-org-custom-rules.md) | `GET /users/current/orgs/:org/custom_rules` | [docs](https://wakatime.com/developers#org_custom_rules) |
| [List Current Org Dashboard Members](actions/list-current-org-dashboard-members.md) | `GET /users/current/orgs/:org/dashboards/:dashboard/members` | [docs](https://wakatime.com/developers#org_dashboard_members) |
| [List Current Org Dashboards](actions/list-current-org-dashboards.md) | `GET /users/current/orgs/:org/dashboards` | [docs](https://wakatime.com/developers#org_dashboards) |
| [List Current Orgs](actions/list-current-orgs.md) | `GET /users/current/orgs` | [docs](https://wakatime.com/developers#orgs) |
| [List Current Private Leaderboards](actions/list-current-private-leaderboards.md) | `GET /users/current/leaderboards` | [docs](https://wakatime.com/developers#private_leaderboards) |
| [List Current Project Commits](actions/list-current-project-commits.md) | `GET /users/current/projects/:project/commits` | [docs](https://wakatime.com/developers#commits) |
| [List Current Projects](actions/list-current-projects.md) | `GET /users/current/projects` | [docs](https://wakatime.com/developers#projects) |
| [List Current Stats](actions/list-current-stats.md) | `GET /users/current/stats` | [docs](https://wakatime.com/developers#stats) |
| [List Current User Agents](actions/list-current-user-agents.md) | `GET /users/current/user_agents` | [docs](https://wakatime.com/developers#user_agents) |
| [List Custom Rules](actions/list-custom-rules.md) | `GET /users/:user/custom_rules` | [docs](https://wakatime.com/developers#custom_rules) |
| [List Data Dumps](actions/list-data-dumps.md) | `GET /users/:user/data_dumps` | [docs](https://wakatime.com/developers#data_dumps) |
| [List Durations](actions/list-durations.md) | `GET /users/:user/durations` | [docs](https://wakatime.com/developers#durations) |
| [List Editors](actions/list-editors.md) | `GET /editors` | [docs](https://wakatime.com/developers#editors) |
| [List External Durations](actions/list-external-durations.md) | `GET /users/:user/external_durations` | [docs](https://wakatime.com/developers#external_durations) |
| [List Goals](actions/list-goals.md) | `GET /users/:user/goals` | [docs](https://wakatime.com/developers#goals) |
| [List Heartbeats](actions/list-heartbeats.md) | `GET /users/:user/heartbeats` | [docs](https://wakatime.com/developers#heartbeats) |
| [List Machine Names](actions/list-machine-names.md) | `GET /users/:user/machine_names` | [docs](https://wakatime.com/developers#machine_names) |
| [List Org Custom Rules](actions/list-org-custom-rules.md) | `GET /users/:user/orgs/:org/custom_rules` | [docs](https://wakatime.com/developers#org_custom_rules) |
| [List Org Dashboard Members](actions/list-org-dashboard-members.md) | `GET /users/:user/orgs/:org/dashboards/:dashboard/members` | [docs](https://wakatime.com/developers#org_dashboard_members) |
| [List Org Dashboards](actions/list-org-dashboards.md) | `GET /users/:user/orgs/:org/dashboards` | [docs](https://wakatime.com/developers#org_dashboards) |
| [List Orgs](actions/list-orgs.md) | `GET /users/:user/orgs` | [docs](https://wakatime.com/developers#orgs) |
| [List Private Leaderboards](actions/list-private-leaderboards.md) | `GET /users/:user/leaderboards` | [docs](https://wakatime.com/developers#private_leaderboards) |
| [List Program Languages](actions/list-program-languages.md) | `GET /program_languages` | [docs](https://wakatime.com/developers#program_languages) |
| [List Project Commits](actions/list-project-commits.md) | `GET /users/:user/projects/:project/commits` | [docs](https://wakatime.com/developers#commits) |
| [List Projects](actions/list-projects.md) | `GET /users/:user/projects` | [docs](https://wakatime.com/developers#projects) |
| [List Public Leaders](actions/list-public-leaders.md) | `GET /leaders` | [docs](https://wakatime.com/developers#leaders) |
| [List Stats](actions/list-stats.md) | `GET /users/:user/stats` | [docs](https://wakatime.com/developers#stats) |
| [List User Agents](actions/list-user-agents.md) | `GET /users/:user/user_agents` | [docs](https://wakatime.com/developers#user_agents) |
| [Upsert Current Custom Rule](actions/upsert-current-custom-rule.md) | `PUT /users/current/custom_rules` | [docs](https://wakatime.com/developers#custom_rules) |
| [Upsert Current Org Custom Rule](actions/upsert-current-org-custom-rule.md) | `PUT /users/current/orgs/:org/custom_rules` | [docs](https://wakatime.com/developers#org_custom_rules) |
| [Upsert Custom Rule](actions/upsert-custom-rule.md) | `PUT /users/:user/custom_rules` | [docs](https://wakatime.com/developers#custom_rules) |
| [Upsert Org Custom Rule](actions/upsert-org-custom-rule.md) | `PUT /users/:user/orgs/:org/custom_rules` | [docs](https://wakatime.com/developers#org_custom_rules) |
