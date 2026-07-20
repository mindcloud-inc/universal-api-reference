# Rollbar: Native API Reference

A consolidated summary of Rollbar's API configuration and 95 documented operations, with links to official documentation.

- **Official docs:** https://docs.rollbar.com/reference/getting-started-1
- **API base URL:** `https://api.rollbar.com/api/1`

## Authentication

### Rollbar Access Token

Custom header auth for Rollbar using X-Rollbar-Access-Token.

### Credentials

- **API Key:** `apiKey` · required · Rollbar access token used in the X-Rollbar-Access-Token header.

Send these headers with each API request:

```http
X-Rollbar-Access-Token: <apiKey>
```

[Official authentication documentation](https://docs.rollbar.com/reference/getting-started-1)

## API conventions

Response data is read from `result`.

## Endpoints (95 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign Team To Project](actions/assign-team-to-project.md) | `PUT /project/:projectId/team/:teamId` | [docs](https://docs.rollbar.com/reference/assign-a-team-to-a-project) |
| [Assign User To Team](actions/assign-user-to-team.md) | `PUT /team/:teamId/user/:userId` | [docs](https://docs.rollbar.com/reference/assign-a-user-to-team) |
| [Cancel Invitation](actions/cancel-invitation.md) | `DELETE /invite/:inviteId` | [docs](https://docs.rollbar.com/reference/cancel-an-invitation) |
| [Cancel RQL Job](actions/cancel-rql-job.md) | `POST /rql/job/:jobId/cancel` | [docs](https://docs.rollbar.com/reference/cancel-an-rql-job) |
| [Check RQL Job](actions/check-rql-job.md) | `GET /rql/job/:jobId` | [docs](https://docs.rollbar.com/reference/get-an-rql-job) |
| [Check Team Assigned To Project](actions/check-team-assigned-to-project.md) | `GET /project/:projectId/team/:teamId` | [docs](https://docs.rollbar.com/reference/check-if-a-team-is-assigned-to-a-project) |
| [Check User In Team](actions/check-user-in-team.md) | `GET /team/:teamId/user/:userId` | [docs](https://docs.rollbar.com/reference/check-if-a-user-is-assigned-to-a-team) |
| [Configure Email Notifications](actions/configure-email-notifications.md) | `PUT /notifications/email` | [docs](https://docs.rollbar.com/reference/put_api-1-notifications-email) |
| [Configure PagerDuty Notifications](actions/configure-pager-duty-notifications.md) | `PUT /notifications/pagerduty` | [docs](https://docs.rollbar.com/reference/put_api-1-notifications-pagerduty) |
| [Configure Slack Notifications](actions/configure-slack-notifications.md) | `PUT /notifications/slack` | [docs](https://docs.rollbar.com/reference/put_api-1-notifications-slack) |
| [Configure Webhook Notifications](actions/configure-webhook-notifications.md) | `PUT /notifications/webhook` | [docs](https://docs.rollbar.com/reference/put_api-1-notifications-webhook) |
| [Create Email Notification Rule](actions/create-email-notification-rule.md) | `POST /notifications/email/rules` | [docs](https://docs.rollbar.com/reference/post_api-1-notifications-email-rules) |
| [Create PagerDuty Notification Rule](actions/create-pager-duty-notification-rule.md) | `POST /notifications/pagerduty` | [docs](https://docs.rollbar.com/reference/post_api-1-notifications-pagerduty-rules) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://docs.rollbar.com/reference/create-a-project) |
| [Create Project Access Token](actions/create-project-access-token.md) | `POST /project/:projectId/access_tokens` | [docs](https://docs.rollbar.com/reference/post_api-1-project-project-id-access-tokens) |
| [Create RQL Job](actions/create-rql-job.md) | `POST /rql/jobs/` | [docs](https://docs.rollbar.com/reference/create-an-rql-job) |
| [Create Service Link](actions/create-service-link.md) | `POST /service_links` | [docs](https://docs.rollbar.com/reference/post_api-1-service-links) |
| [Create Slack Notification Rule](actions/create-slack-notification-rule.md) | `POST /notifications/slack/rules` | [docs](https://docs.rollbar.com/reference/post_api-1-notifications-slack-rules) |
| [Create Team](actions/create-team.md) | `POST /teams` | [docs](https://docs.rollbar.com/reference/create-a-team) |
| [Create Webhook Notification Rule](actions/create-webhook-notification-rule.md) | `POST /notifications/webhook/rules` | [docs](https://docs.rollbar.com/reference/post_api-1-notifications-webhook-rules) |
| [Delete Email Notification Rule](actions/delete-email-notification-rule.md) | `DELETE /notifications/email/rule/:ruleId` | [docs](https://docs.rollbar.com/reference/delete_api-1-notifications-email-rule-rule-id) |
| [Delete Occurrence](actions/delete-occurrence.md) | `DELETE /instance/:instanceId` | [docs](https://docs.rollbar.com/reference/delete_api-1-instance-instance-id) |
| [Delete PagerDuty Notification Rule](actions/delete-pager-duty-notification-rule.md) | `DELETE /notifications/pagerduty/rule/:ruleId` | [docs](https://docs.rollbar.com/reference/delete_api-1-notifications-pagerduty-rule-rule-id) |
| [Delete Project](actions/delete-project.md) | `DELETE /project/:projectId` | [docs](https://docs.rollbar.com/reference/delete-a-project) |
| [Delete Project Access Token By Body](actions/delete-project-access-token-by-body.md) | `DELETE /project/:projectId/access_token` | [docs](https://docs.rollbar.com/reference/delete-a-project-access-token) |
| [Delete Project Access Token By Path](actions/delete-project-access-token-by-path.md) | `DELETE /project/:projectId/access_token/:tokenIdentifier` | [docs](https://docs.rollbar.com/reference/delete-a-project-access-token) |
| [Delete Service Link](actions/delete-service-link.md) | `DELETE /service_links/:id` | [docs](https://docs.rollbar.com/reference/delete_api-1-service-links-id) |
| [Delete Session Replay](actions/delete-session-replay.md) | `DELETE /environment/:environment/session/:sessionId/replay/:replayId` | [docs](https://docs.rollbar.com/reference/delete-a-replay) |
| [Delete Slack Notification Rule](actions/delete-slack-notification-rule.md) | `DELETE /notifications/slack/rule/:ruleId` | [docs](https://docs.rollbar.com/reference/delete_api-1-notifications-slack-rule-rule-id) |
| [Delete Team](actions/delete-team.md) | `DELETE /team/:teamId` | [docs](https://docs.rollbar.com/reference/delete-a-team) |
| [Delete Webhook Notification Rule](actions/delete-webhook-notification-rule.md) | `DELETE /notifications/webhook/rule/:ruleId` | [docs](https://docs.rollbar.com/reference/delete_api-1-notifications-webhook-rule-rule-id) |
| [Get Activated Item Counts](actions/get-activated-item-counts.md) | `GET /reports/activated_counts` | [docs](https://docs.rollbar.com/reference/get-activated-item-counts) |
| [Get Deploy](actions/get-deploy.md) | `GET /deploy/:deployId` | [docs](https://docs.rollbar.com/reference/get-a-deploy) |
| [Get Email Notification Rule](actions/get-email-notification-rule.md) | `GET /notifications/email/rule/:ruleId` | [docs](https://docs.rollbar.com/reference/get_api-1-notifications-email-rule-rule-id) |
| [Get Invitation](actions/get-invitation.md) | `GET /invite/:inviteId` | [docs](https://docs.rollbar.com/reference/get-an-invitation) |
| [Get Item](actions/get-item.md) | `GET /item/:itemId` | [docs](https://docs.rollbar.com/reference/get-an-item-by-id) |
| [Get Item By Counter](actions/get-item-by-counter.md) | `GET /item_by_counter/:counter` | [docs](https://docs.rollbar.com/reference/get-an-item-by-project-counter) |
| [Get Item By UUID](actions/get-item-by-uuid.md) | `GET /item/` | [docs](https://docs.rollbar.com/reference/get-an-item-by-occurrence-uuid) |
| [Get Item Metrics](actions/get-item-metrics.md) | `POST /metrics/items` | [docs](https://docs.rollbar.com/reference/post_api-1-metrics-items) |
| [Get Occurrence](actions/get-occurrence.md) | `GET /instance/:instanceId` | [docs](https://docs.rollbar.com/reference/get_api-1-instance-instance-id) |
| [Get Occurrence Counts](actions/get-occurrence-counts.md) | `GET /reports/occurrence_counts` | [docs](https://docs.rollbar.com/reference/get-occurrence-counts) |
| [Get Occurrence Metrics](actions/get-occurrence-metrics.md) | `POST /metrics/occurrences` | [docs](https://docs.rollbar.com/reference/post_api-1-metrics-occurrences) |
| [Get PagerDuty Notification Rule](actions/get-pager-duty-notification-rule.md) | `GET /notifications/pagerduty/rule/:ruleId` | [docs](https://docs.rollbar.com/reference/get_api-1-notifications-pagerduty-rule-rule-id) |
| [Get Person Deletion Status](actions/get-person-deletion-status.md) | `GET /people/delete_jobs/:jobId` | [docs](https://docs.rollbar.com/reference/get-person-deletion-status) |
| [Get Project](actions/get-project.md) | `GET /project/:projectId` | [docs](https://docs.rollbar.com/reference/get-a-project) |
| [Get Resolution Time Metrics](actions/get-resolution-time-metrics.md) | `POST /metrics/ttr` | [docs](https://docs.rollbar.com/reference/post_api-1-metrics-ttr) |
| [Get RQL Job Results](actions/get-rql-job-results.md) | `GET /rql/job/:jobId/result` | [docs](https://docs.rollbar.com/reference/get-rql-job-results) |
| [Get Service Link](actions/get-service-link.md) | `GET /service_links/:id` | [docs](https://docs.rollbar.com/reference/get_api-1-service-links-id) |
| [Get Session Replay](actions/get-session-replay.md) | `GET /environment/:environment/session/:sessionId/replay/:replayId` | [docs](https://docs.rollbar.com/reference/get-a-replay) |
| [Get Slack Notification Rule](actions/get-slack-notification-rule.md) | `GET /notifications/slack/rule/:ruleId` | [docs](https://docs.rollbar.com/reference/get_api-1-notifications-slack-rule-rule-id) |
| [Get Team](actions/get-team.md) | `GET /team/:teamId` | [docs](https://docs.rollbar.com/reference/get-a-team) |
| [Get Top Active Items](actions/get-top-active-items.md) | `GET /reports/top_active_items` | [docs](https://docs.rollbar.com/reference/get-top-active-items) |
| [Get User](actions/get-user.md) | `GET /user/:userId` | [docs](https://docs.rollbar.com/reference/get-a-user) |
| [Get Version Details](actions/get-version-details.md) | `GET /versions/:version` | [docs](https://docs.rollbar.com/reference/get_api-1-versions-version) |
| [Get Webhook Notification Rule](actions/get-webhook-notification-rule.md) | `GET /notifications/webhook/rule/:ruleId` | [docs](https://docs.rollbar.com/reference/get_api-1-notifications-webhook-rule-rule-id) |
| [Invite Email To Team](actions/invite-email-to-team.md) | `POST /team/:teamId/invites` | [docs](https://docs.rollbar.com/reference/invite-an-email-address-to-a-team) |
| [List Deploys](actions/list-deploys.md) | `GET /deploys` | [docs](https://docs.rollbar.com/reference/list-all-deploys) |
| [List Email Notification Rules](actions/list-email-notification-rules.md) | `GET /notifications/email/rules` | [docs](https://docs.rollbar.com/reference/get_api-1-notifications-email-rules) |
| [List Environments](actions/list-environments.md) | `GET /environments` | [docs](https://docs.rollbar.com/reference/list-all-environments) |
| [List Item Occurrences](actions/list-item-occurrences.md) | `GET /item/:itemId/instances` | [docs](https://docs.rollbar.com/reference/get_api-1-item-item-id-instances) |
| [List Items](actions/list-items.md) | `GET /items` | [docs](https://docs.rollbar.com/reference/list-all-items) |
| [List PagerDuty Notification Rules](actions/list-pager-duty-notification-rules.md) | `GET /notifications/pagerduty/rules` | [docs](https://docs.rollbar.com/reference/get_api-1-notifications-pagerduty-rules) |
| [List Project Access Tokens](actions/list-project-access-tokens.md) | `GET /project/:projectId/access_tokens` | [docs](https://docs.rollbar.com/reference/list-all-project-access-tokens) |
| [List Project Occurrences](actions/list-project-occurrences.md) | `GET /instances` | [docs](https://docs.rollbar.com/reference/get_api-1-instances) |
| [List Project Teams](actions/list-project-teams.md) | `GET /project/:projectId/teams` | [docs](https://docs.rollbar.com/reference/list-a-projects-teams) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://docs.rollbar.com/reference/list-all-projects) |
| [List RQL Jobs](actions/list-rql-jobs.md) | `GET /rql/jobs/` | [docs](https://docs.rollbar.com/reference/list-rql-jobs) |
| [List Service Links](actions/list-service-links.md) | `GET /service_links` | [docs](https://docs.rollbar.com/reference/get_api-1-service-links) |
| [List Slack Notification Rules](actions/list-slack-notification-rules.md) | `GET /notifications/slack/rules` | [docs](https://docs.rollbar.com/reference/get_api-1-notifications-slack-rules) |
| [List Team Invitations](actions/list-team-invitations.md) | `GET /team/:teamId/invites` | [docs](https://docs.rollbar.com/reference/list-invitations-for-a-team) |
| [List Team Projects](actions/list-team-projects.md) | `GET /team/:teamId/projects` | [docs](https://docs.rollbar.com/reference/list-a-teams-projects) |
| [List Team Users](actions/list-team-users.md) | `GET /team/:teamId/users` | [docs](https://docs.rollbar.com/reference/list-a-teams-users) |
| [List Teams](actions/list-teams.md) | `GET /teams` | [docs](https://docs.rollbar.com/reference/list-all-teams) |
| [List User Projects](actions/list-user-projects.md) | `GET /user/:userId/projects` | [docs](https://docs.rollbar.com/reference/list-a-users-projects) |
| [List User Teams](actions/list-user-teams.md) | `GET /user/:userId/teams` | [docs](https://docs.rollbar.com/reference/list-a-users-teams) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://docs.rollbar.com/reference/list-all-users) |
| [List Version Items](actions/list-version-items.md) | `GET /versions/:version/items` | [docs](https://docs.rollbar.com/reference/get_api-1-versions-version-items) |
| [List Webhook Notification Rules](actions/list-webhook-notification-rules.md) | `GET /notifications/webhook/rules` | [docs](https://docs.rollbar.com/reference/get_api-1-notifications-webhook-rules) |
| [Remove Team From Project](actions/remove-team-from-project.md) | `DELETE /project/:projectId/team/:teamId` | [docs](https://docs.rollbar.com/reference/remove-a-team-from-a-project) |
| [Remove User From Team](actions/remove-user-from-team.md) | `DELETE /team/:teamId/user/:userId` | [docs](https://docs.rollbar.com/reference/remove-a-user-from-a-team) |
| [Replace Email Notification Rules](actions/replace-email-notification-rules.md) | `PUT /notifications/email/rules` | [docs](https://docs.rollbar.com/reference/put_api-1-notifications-email-rules) |
| [Replace PagerDuty Notification Rules](actions/replace-pager-duty-notification-rules.md) | `PUT /notifications/pagerduty/rules` | [docs](https://docs.rollbar.com/reference/put_api-1-notifications-pagerduty-rules) |
| [Replace Slack Notification Rules](actions/replace-slack-notification-rules.md) | `PUT /notifications/slack/rules` | [docs](https://docs.rollbar.com/reference/put_api-1-notifications-slack-rules) |
| [Replace Webhook Notification Rules](actions/replace-webhook-notification-rules.md) | `PUT /notifications/webhook/rules` | [docs](https://docs.rollbar.com/reference/put_api-1-notifications-webhook-rules) |
| [Report Deploy](actions/report-deploy.md) | `POST /deploy` | [docs](https://docs.rollbar.com/reference/post-deploy) |
| [Request Person Deletion](actions/request-person-deletion.md) | `POST /people/delete_jobs/` | [docs](https://docs.rollbar.com/reference/request-person-deletion) |
| [Update Access Token Rate Limit By Body](actions/update-access-token-rate-limit-by-body.md) | `PATCH /project/:projectId/access_token` | [docs](https://docs.rollbar.com/reference/update-a-rate-limit) |
| [Update Access Token Rate Limit By Path](actions/update-access-token-rate-limit-by-path.md) | `PATCH /project/:projectId/access_token/:tokenIdentifier` | [docs](https://docs.rollbar.com/reference/update-a-rate-limit) |
| [Update Deploy](actions/update-deploy.md) | `PATCH /deploy/:deployId` | [docs](https://docs.rollbar.com/reference/update-a-deploy) |
| [Update Email Notification Rule](actions/update-email-notification-rule.md) | `PUT /notifications/email/rule/:ruleId` | [docs](https://docs.rollbar.com/reference/put_api-1-notifications-email-rule-rule-id) |
| [Update Item](actions/update-item.md) | `PATCH /item/:itemId` | [docs](https://docs.rollbar.com/reference/update-an-item) |
| [Update PagerDuty Notification Rule](actions/update-pager-duty-notification-rule.md) | `PUT /notifications/pagerduty/rule/:ruleId` | [docs](https://docs.rollbar.com/reference/put_api-1-notifications-pagerduty-rule-rule-id) |
| [Update Service Link](actions/update-service-link.md) | `PUT /service_links/:id` | [docs](https://docs.rollbar.com/reference/put_api-1-service-links-id) |
| [Update Slack Notification Rule](actions/update-slack-notification-rule.md) | `PUT /notifications/slack/rule/:ruleId` | [docs](https://docs.rollbar.com/reference/put_api-1-notifications-slack-rule-rule-id) |
| [Update Webhook Notification Rule](actions/update-webhook-notification-rule.md) | `PUT /notifications/webhook/rule/:ruleId` | [docs](https://docs.rollbar.com/reference/put_api-1-notifications-webhook-rule-rule-id) |
