# <img src="https://images.mindcloud.co/apps/icons/rollbar-icon-square_1775840441619.png" alt="Rollbar logo" width="28" height="28"> Rollbar: Universal API

Observability API wrapper for Rollbar projects, items, occurrences, deploys, environments, teams, users, reports, notification rules, service links, and versions.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rollbar/latest
- **Category:** IT Operations / Observability
- **Actions:** 95
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://rollbar.com
- **Vendor API docs:** https://docs.rollbar.com/reference/getting-started-1

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check RQL Job](actions/check-rql-job.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rollbar/latest/actions/check-rql-job?connectionId=$CONNECTION_ID&jobId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (95)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Create Project Access Token](actions/create-project-access-token.md) | POST | Creates a new project access token in Rollbar. |
| [Delete Project Access Token By Body](actions/delete-project-access-token-by-body.md) | DELETE | Deletes a project access token from Rollbar by body identifier. |
| [Delete Project Access Token By Path](actions/delete-project-access-token-by-path.md) | DELETE | Deletes a project access token from Rollbar by path identifier. |
| [List Project Access Tokens](actions/list-project-access-tokens.md) | GET | Retrieves project access tokens from Rollbar. |
| [Update Access Token Rate Limit By Body](actions/update-access-token-rate-limit-by-body.md) | PUT | Updates a project access token rate limit in Rollbar by body identifier. |
| [Update Access Token Rate Limit By Path](actions/update-access-token-rate-limit-by-path.md) | PUT | Updates a project access token rate limit in Rollbar by path identifier. |

### Deployments

| Action | Method | Description |
| --- | --- | --- |
| [Get Deploy](actions/get-deploy.md) | GET | Retrieves a deploy from Rollbar. |
| [List Deploys](actions/list-deploys.md) | GET | Retrieves deploys from Rollbar. |
| [Report Deploy](actions/report-deploy.md) | POST | Creates a new deploy in Rollbar. |
| [Update Deploy](actions/update-deploy.md) | PUT | Updates an existing deploy in Rollbar. |

### Environments

| Action | Method | Description |
| --- | --- | --- |
| [Delete Session Replay](actions/delete-session-replay.md) | DELETE | Deletes an existing session replay from Rollbar. |
| [Get Session Replay](actions/get-session-replay.md) | GET | Retrieves a session replay from Rollbar. |
| [List Environments](actions/list-environments.md) | GET | Retrieves environments from Rollbar. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Cancel RQL Job](actions/cancel-rql-job.md) | PUT | Cancels an RQL job in Rollbar. |
| [Check RQL Job](actions/check-rql-job.md) | GET | Retrieves an RQL job from Rollbar. |
| [Create RQL Job](actions/create-rql-job.md) | POST | Creates a new RQL job in Rollbar. |
| [Delete Occurrence](actions/delete-occurrence.md) | DELETE | Deletes an existing occurrence from Rollbar. |
| [Get Activated Item Counts](actions/get-activated-item-counts.md) | GET | Retrieves activated item counts from Rollbar. |
| [Get Item](actions/get-item.md) | GET | Retrieves an item from Rollbar. |
| [Get Item By Counter](actions/get-item-by-counter.md) | GET | Retrieves an item from Rollbar by project counter. |
| [Get Item By UUID](actions/get-item-by-uuid.md) | GET | Retrieves an item from Rollbar by occurrence UUID. |
| [Get Item Metrics](actions/get-item-metrics.md) | GET | Retrieves item metrics from Rollbar. |
| [Get Occurrence](actions/get-occurrence.md) | GET | Retrieves an occurrence from Rollbar. |
| [Get Occurrence Counts](actions/get-occurrence-counts.md) | GET | Retrieves occurrence counts from Rollbar. |
| [Get Occurrence Metrics](actions/get-occurrence-metrics.md) | GET | Retrieves occurrence metrics from Rollbar. |
| [Get RQL Job Results](actions/get-rql-job-results.md) | GET | Retrieves RQL job results from Rollbar. |
| [Get Top Active Items](actions/get-top-active-items.md) | GET | Retrieves top active items from Rollbar. |
| [Get Version Details](actions/get-version-details.md) | GET | Retrieves version details from Rollbar. |
| [List Item Occurrences](actions/list-item-occurrences.md) | GET | Retrieves item occurrences from Rollbar. |
| [List Items](actions/list-items.md) | GET | Retrieves items from Rollbar. |
| [List Project Occurrences](actions/list-project-occurrences.md) | GET | Retrieves project occurrences from Rollbar. |
| [List RQL Jobs](actions/list-rql-jobs.md) | GET | Retrieves RQL jobs from Rollbar. |
| [List Version Items](actions/list-version-items.md) | GET | Retrieves version items from Rollbar. |
| [Update Item](actions/update-item.md) | PUT | Updates an existing item in Rollbar. |

### Memberships

| Action | Method | Description |
| --- | --- | --- |
| [Assign Team To Project](actions/assign-team-to-project.md) | PUT | Assigns a team to a project in Rollbar. |
| [Assign User To Team](actions/assign-user-to-team.md) | PUT | Assigns a user to a team in Rollbar. |
| [Check Team Assigned To Project](actions/check-team-assigned-to-project.md) | GET | Retrieves whether a team is assigned to a Rollbar project. |
| [Check User In Team](actions/check-user-in-team.md) | GET | Retrieves whether a user belongs to a Rollbar team. |
| [Remove Team From Project](actions/remove-team-from-project.md) | DELETE | Removes a team from a project in Rollbar. |
| [Remove User From Team](actions/remove-user-from-team.md) | DELETE | Removes a user from a team in Rollbar. |

### Notifications

| Action | Method | Description |
| --- | --- | --- |
| [Configure Email Notifications](actions/configure-email-notifications.md) | PUT | Updates email notification settings in Rollbar. |
| [Configure PagerDuty Notifications](actions/configure-pager-duty-notifications.md) | PUT | Updates PagerDuty notification settings in Rollbar. |
| [Configure Slack Notifications](actions/configure-slack-notifications.md) | PUT | Updates Slack notification settings in Rollbar. |
| [Configure Webhook Notifications](actions/configure-webhook-notifications.md) | PUT | Updates webhook notification settings in Rollbar. |
| [Create Email Notification Rule](actions/create-email-notification-rule.md) | POST | Creates an email notification rule in Rollbar. |
| [Create PagerDuty Notification Rule](actions/create-pager-duty-notification-rule.md) | POST | Creates a PagerDuty notification rule in Rollbar. |
| [Create Slack Notification Rule](actions/create-slack-notification-rule.md) | POST | Creates a Slack notification rule in Rollbar. |
| [Create Webhook Notification Rule](actions/create-webhook-notification-rule.md) | POST | Creates a webhook notification rule in Rollbar. |
| [Delete Email Notification Rule](actions/delete-email-notification-rule.md) | DELETE | Deletes an email notification rule from Rollbar. |
| [Delete PagerDuty Notification Rule](actions/delete-pager-duty-notification-rule.md) | DELETE | Deletes a PagerDuty notification rule from Rollbar. |
| [Delete Slack Notification Rule](actions/delete-slack-notification-rule.md) | DELETE | Deletes a Slack notification rule from Rollbar. |
| [Delete Webhook Notification Rule](actions/delete-webhook-notification-rule.md) | DELETE | Deletes a webhook notification rule from Rollbar. |
| [Get Email Notification Rule](actions/get-email-notification-rule.md) | GET | Retrieves an email notification rule from Rollbar. |
| [Get PagerDuty Notification Rule](actions/get-pager-duty-notification-rule.md) | GET | Retrieves a PagerDuty notification rule from Rollbar. |
| [Get Slack Notification Rule](actions/get-slack-notification-rule.md) | GET | Retrieves a Slack notification rule from Rollbar. |
| [Get Webhook Notification Rule](actions/get-webhook-notification-rule.md) | GET | Retrieves a webhook notification rule from Rollbar. |
| [List Email Notification Rules](actions/list-email-notification-rules.md) | GET | Retrieves email notification rules from Rollbar. |
| [List PagerDuty Notification Rules](actions/list-pager-duty-notification-rules.md) | GET | Retrieves PagerDuty notification rules from Rollbar. |
| [List Slack Notification Rules](actions/list-slack-notification-rules.md) | GET | Retrieves Slack notification rules from Rollbar. |
| [List Webhook Notification Rules](actions/list-webhook-notification-rules.md) | GET | Retrieves webhook notification rules from Rollbar. |
| [Replace Email Notification Rules](actions/replace-email-notification-rules.md) | PUT | Updates email notification rules in Rollbar. |
| [Replace PagerDuty Notification Rules](actions/replace-pager-duty-notification-rules.md) | PUT | Updates PagerDuty notification rules in Rollbar. |
| [Replace Slack Notification Rules](actions/replace-slack-notification-rules.md) | PUT | Updates Slack notification rules in Rollbar. |
| [Replace Webhook Notification Rules](actions/replace-webhook-notification-rules.md) | PUT | Updates webhook notification rules in Rollbar. |
| [Update Email Notification Rule](actions/update-email-notification-rule.md) | PUT | Updates an email notification rule in Rollbar. |
| [Update PagerDuty Notification Rule](actions/update-pager-duty-notification-rule.md) | PUT | Updates a PagerDuty notification rule in Rollbar. |
| [Update Slack Notification Rule](actions/update-slack-notification-rule.md) | PUT | Updates a Slack notification rule in Rollbar. |
| [Update Webhook Notification Rule](actions/update-webhook-notification-rule.md) | PUT | Updates a webhook notification rule in Rollbar. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Rollbar. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from Rollbar. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Rollbar. |
| [Get Resolution Time Metrics](actions/get-resolution-time-metrics.md) | GET | Retrieves resolution time metrics from Rollbar. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Rollbar. |
| [List Team Projects](actions/list-team-projects.md) | GET | Retrieves projects for a Rollbar team. |
| [List User Projects](actions/list-user-projects.md) | GET | Retrieves projects for a Rollbar user. |

### Services

| Action | Method | Description |
| --- | --- | --- |
| [Create Service Link](actions/create-service-link.md) | POST | Creates a new service link in Rollbar. |
| [Delete Service Link](actions/delete-service-link.md) | DELETE | Deletes an existing service link from Rollbar. |
| [Get Service Link](actions/get-service-link.md) | GET | Retrieves a service link from Rollbar. |
| [List Service Links](actions/list-service-links.md) | GET | Retrieves service links from Rollbar. |
| [Update Service Link](actions/update-service-link.md) | PUT | Updates an existing service link in Rollbar. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Invitation](actions/cancel-invitation.md) | DELETE | Deletes an existing team invitation from Rollbar. |
| [Create Team](actions/create-team.md) | POST | Creates a new team in Rollbar. |
| [Delete Team](actions/delete-team.md) | DELETE | Deletes an existing team from Rollbar. |
| [Get Invitation](actions/get-invitation.md) | GET | Retrieves a team invitation from Rollbar. |
| [Get Team](actions/get-team.md) | GET | Retrieves a team from Rollbar. |
| [Invite Email To Team](actions/invite-email-to-team.md) | POST | Creates a team invitation in Rollbar. |
| [List Project Teams](actions/list-project-teams.md) | GET | Retrieves teams for a Rollbar project. |
| [List Team Invitations](actions/list-team-invitations.md) | GET | Retrieves team invitations from Rollbar. |
| [List Teams](actions/list-teams.md) | GET | Retrieves teams from Rollbar. |
| [List User Teams](actions/list-user-teams.md) | GET | Retrieves teams for a Rollbar user. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Person Deletion Status](actions/get-person-deletion-status.md) | GET | Retrieves person deletion status from Rollbar. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Rollbar. |
| [List Team Users](actions/list-team-users.md) | GET | Retrieves users assigned to a Rollbar team. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Rollbar. |
| [Request Person Deletion](actions/request-person-deletion.md) | POST | Creates a person deletion request in Rollbar. |

