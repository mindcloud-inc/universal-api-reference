# Dashcam: Native API Reference

A consolidated summary of Dashcam's API configuration and 47 documented operations, with links to official documentation.

- **Official docs:** https://docs.testdriver.ai
- **OpenAPI specification:** https://console.testdriver.ai/js/sdk/cloud.setup.js?v=2
- **API base URL:** `https://api.testdriver.ai`

## Authentication

### Dashcam Bearer Token

Use a Dashcam bearer token generated from TestDriver's API-key exchange flow.

### Credentials

- **Bearer Token:** `token` · required · Paste the Dashcam bearer token returned by POST https://api.testdriver.ai/auth/exchange-api-key.

Send these headers with each API request:

```http
Authorization: Bearer <token>
```

[Official authentication documentation](https://docs.testdriver.ai/v6/account/team)

## Endpoints (47 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Clear Cache](actions/clear-cache.md) | `DELETE /api/v1/cache/clear` | [docs](https://docs.testdriver.ai) |
| [Clone Replay](actions/clone-replay.md) | `PUT /api/v1/replay/:replayId/clone` | [docs](https://docs.testdriver.ai/v7/api/dashcam) |
| [Create Checkout Session](actions/create-checkout-session.md) | `POST /api/billing/checkout` | [docs](https://docs.testdriver.ai/v6/account/team) |
| [Create Comment](actions/create-comment.md) | `POST /api/v1/comment` | [docs](https://docs.testdriver.ai/v7/api/dashcam) |
| [Create Project](actions/create-project.md) | `POST /api/v1/project` | [docs](https://docs.testdriver.ai/v6/account/dashboard) |
| [Delete Cache By Prompt](actions/delete-cache-by-prompt.md) | `DELETE /api/v1/cache/by-prompt` | [docs](https://docs.testdriver.ai) |
| [Delete Cache Entry](actions/delete-cache-entry.md) | `DELETE /api/v1/cache/entry` | [docs](https://docs.testdriver.ai) |
| [Delete Comment](actions/delete-comment.md) | `DELETE /api/v1/comment` | [docs](https://docs.testdriver.ai/v7/api/dashcam) |
| [Delete Project](actions/delete-project.md) | `DELETE /api/v1/projects/:id` | [docs](https://docs.testdriver.ai/v6/account/dashboard) |
| [Delete Replay](actions/delete-replay.md) | `DELETE /api/v1/replay/:replayId` | [docs](https://docs.testdriver.ai/v7/api/dashcam) |
| [Delete Replay Access](actions/delete-replay-access.md) | `DELETE /api/v1/replay/:replayId/access-delete` | [docs](https://docs.testdriver.ai/v7/api/dashcam) |
| [Download Build](actions/download-build.md) | `GET /api/v1/download` | [docs](https://docs.testdriver.ai/v7/api/dashcam) |
| [Download Log](actions/download-log.md) | `GET /api/v1/logs/:logId/download` | [docs](https://docs.testdriver.ai/v7/api/dashcam) |
| [Download Replay Performance](actions/download-replay-performance.md) | `GET /api/v1/replay/:replayId/performance` | [docs](https://docs.testdriver.ai/v7/api/dashcam) |
| [Get Billing Usage](actions/get-billing-usage.md) | `GET /api/billing/usage` | [docs](https://docs.testdriver.ai/v6/account/team) |
| [Get Cache Entry Interactions](actions/get-cache-entry-interactions.md) | `GET /api/v1/cache/entry/interactions` | [docs](https://docs.testdriver.ai) |
| [Get Coverage Report](actions/get-coverage-report.md) | `GET /api/v1/testdriver/coverage/report` | [docs](https://docs.testdriver.ai/v6/getting-started/ci) |
| [Get Current User](actions/get-current-user.md) | `GET /api/v1/whoami` | [docs](https://docs.testdriver.ai/v6/account/team) |
| [Get Parallel Slots](actions/get-parallel-slots.md) | `GET /api/billing/parallel-slots` | [docs](https://docs.testdriver.ai/v6/account/team) |
| [Get Portal Session](actions/get-portal-session.md) | `GET /api/billing/portal` | [docs](https://docs.testdriver.ai/v6/account/team) |
| [Get Public Stats](actions/get-public-stats.md) | `GET /api/v1/public/stats` | [docs](https://docs.testdriver.ai/v6/account/dashboard) |
| [Get Replay](actions/get-replay.md) | `GET /api/v1/replay` | [docs](https://docs.testdriver.ai/v7/api/dashcam) |
| [Get Replay Interactions](actions/get-replay-interactions.md) | `GET /api/v1/testdriver/interactions` | [docs](https://docs.testdriver.ai/v6/getting-started/ci) |
| [Get Replay Test Cases](actions/get-replay-test-cases.md) | `GET /api/v7.0.0/testdriver/test-cases-by-replay` | [docs](https://docs.testdriver.ai/v6/getting-started/ci) |
| [Get Team](actions/get-team.md) | `GET /api/v1/teams` | [docs](https://docs.testdriver.ai/v6/account/team) |
| [Get Test Case Interactions](actions/get-test-case-interactions.md) | `GET /api/v1/testdriver/interactions/testcase/:testCaseId` | [docs](https://docs.testdriver.ai/v6/getting-started/ci) |
| [Get Testdriver Stats](actions/get-testdriver-stats.md) | `GET /api/v1/testdriver-stats` | [docs](https://docs.testdriver.ai/v6/getting-started/ci) |
| [Invite Replay Access](actions/invite-replay-access.md) | `PUT /api/v1/replay/:replayId/access-invite` | [docs](https://docs.testdriver.ai/v7/api/dashcam) |
| [Invite Team Member](actions/invite-team-member.md) | `POST /api/v1/teams/invite-member` | [docs](https://docs.testdriver.ai/v6/account/team) |
| [List Cache Entries](actions/list-cache-entries.md) | `GET /api/v1/cache/entries` | [docs](https://docs.testdriver.ai) |
| [List Comments](actions/list-comments.md) | `GET /api/v1/comment` | [docs](https://docs.testdriver.ai/v7/api/dashcam) |
| [List Projects](actions/list-projects.md) | `GET /api/v1/projects` | [docs](https://docs.testdriver.ai/v6/account/dashboard) |
| [List Replays](actions/list-replays.md) | `GET /api/v1/replays` | [docs](https://docs.testdriver.ai/v7/api/dashcam) |
| [List Testdriver Results](actions/list-testdriver-results.md) | `GET /api/v1/testdriver-results` | [docs](https://docs.testdriver.ai/v6/getting-started/ci) |
| [List Testdriver Suites](actions/list-testdriver-suites.md) | `GET /api/v1/testdriver-suites` | [docs](https://docs.testdriver.ai/v6/getting-started/ci) |
| [List Usage Records](actions/list-usage-records.md) | `GET /api/billing/usage-records` | [docs](https://docs.testdriver.ai/v6/account/team) |
| [Mark Replay Viewed](actions/mark-replay-viewed.md) | `POST /api/v1/replay/view-notification` | [docs](https://docs.testdriver.ai/v7/api/dashcam) |
| [Move Replay](actions/move-replay.md) | `PUT /api/v1/replay/:replayId/move` | [docs](https://docs.testdriver.ai/v7/api/dashcam) |
| [Publish Replay](actions/publish-replay.md) | `POST /api/v1/replay/publish` | [docs](https://docs.testdriver.ai/v7/api/dashcam) |
| [Remove Pending Invite](actions/remove-pending-invite.md) | `DELETE /api/v1/teams/pending-invite-delete` | [docs](https://docs.testdriver.ai/v6/account/team) |
| [Remove Team Member](actions/remove-team-member.md) | `DELETE /api/v1/teams/member-delete` | [docs](https://docs.testdriver.ai/v6/account/team) |
| [Request Replay Access](actions/request-replay-access.md) | `POST /api/v1/replay/:replayId/access-request` | [docs](https://docs.testdriver.ai/v7/api/dashcam) |
| [Save Replay Draft](actions/save-replay-draft.md) | `POST /api/v1/replay/draft` | [docs](https://docs.testdriver.ai/v7/api/dashcam) |
| [Update Project](actions/update-project.md) | `PUT /api/v1/projects/:id` | [docs](https://docs.testdriver.ai/v6/account/dashboard) |
| [Update Replay Access](actions/update-replay-access.md) | `PUT /api/v1/teams/replay-access` | [docs](https://docs.testdriver.ai/v6/account/team) |
| [Update Team Auto Join](actions/update-team-auto-join.md) | `PUT /api/v1/teams/auto-join` | [docs](https://docs.testdriver.ai/v6/account/team) |
| [Update Team Name](actions/update-team-name.md) | `PUT /api/v1/teams/edit-name` | [docs](https://docs.testdriver.ai/v6/account/team) |
