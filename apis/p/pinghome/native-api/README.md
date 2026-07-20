# Pinghome: Native API Reference

A consolidated summary of Pinghome's API configuration and 72 documented operations, with links to official documentation.

- **Official docs:** https://docs.pinghome.io/
- **API base URL:** `https://api.pinghome.io`

## Authentication

### Bearer Token

Use a Pinghome bearer access token returned by the Account Sign In endpoint.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.pinghome.io/authentication/account-signin/)

## API conventions

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size. Use `last_received_at` in the query string as the pagination cursor.

## Endpoints (72 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Change Uptime Monitor Status](actions/change-uptime-monitor-status.md) | `PUT /resource-cmd/v1/resource/:id/status` | [docs](https://docs.pinghome.io/monitoring/uptime-monitoring/change-uptime-monitor-status/) |
| [Check Service Health Status](actions/check-service-health-status.md) | `GET /incident-query/v1/health-check` | [docs](https://docs.pinghome.io/incident-management/incident-tracking/check-service-health-status/) |
| [Create Incident](actions/create-incident.md) | `POST /incident-cmd/v1/team/:id/incident` | [docs](https://docs.pinghome.io/incident-management/incident-tracking/create-incident/) |
| [Create Oncall Schedule](actions/create-oncall-schedule.md) | `POST /incident-cmd/v1/team/:id/schedule` | [docs](https://docs.pinghome.io/incident-management/incident-schedule-management/create-oncall-schedule/) |
| [Create Personal Notification Channel](actions/create-personal-notification-channel.md) | `POST /customer-cmd/v1/customer/:id/notification-channel` | [docs](https://docs.pinghome.io/customer-account-management/account-settings/create-personal-notification-channel/) |
| [Create Ruleset](actions/create-ruleset.md) | `POST https://incident-cmd.api.pinghome.io/v1/ruleset` | [docs](https://docs.pinghome.io/incident-management/ruleset-management-and-event-handling/create-ruleset/) |
| [Create Service](actions/create-service.md) | `POST /resource-cmd/v1/service` | [docs](https://docs.pinghome.io/customer-account-management/team-organization-and-role-setup/create-service/) |
| [Create Statuspage](actions/create-statuspage.md) | `POST /statuspage-cmd/v1/statuspage` | [docs](https://docs.pinghome.io/statuspages/create-statuspage/) |
| [Create Subscription For Statuspages](actions/create-subscription-for-statuspages.md) | `POST /statuspage-cmd/v1/subscriptions` | [docs](https://docs.pinghome.io/statuspages/create-subscription-for-statuspages/) |
| [Create Team](actions/create-team.md) | `POST /customer-cmd/v1/team` | [docs](https://docs.pinghome.io/customer-account-management/team-organization-and-role-setup/create-team/) |
| [Create Team Notification Channel](actions/create-team-notification-channel.md) | `POST /customer-cmd/v1/team/:id/notification-channel` | [docs](https://docs.pinghome.io/customer-account-management/team-organization-and-role-setup/create-team-notification-channel/) |
| [Create Uptime Monitor](actions/create-uptime-monitor.md) | `POST /resource-cmd/v1/resource` | [docs](https://docs.pinghome.io/monitoring/uptime-monitoring/create-uptime-monitor/) |
| [Create Webhook](actions/create-webhook.md) | `POST /incident-cmd/v1/webhook` | [docs](https://docs.pinghome.io/incident-management/ruleset-management-and-event-handling/create-webhook/) |
| [Delete Oncall Schedule](actions/delete-oncall-schedule.md) | `DELETE /incident-cmd/v1/team/:id/schedule` | [docs](https://docs.pinghome.io/incident-management/incident-schedule-management/delete-oncall-schedule/) |
| [Delete Personal Notification Channel](actions/delete-personal-notification-channel.md) | `DELETE /customer-cmd/v1/customer/:id/notification-channel` | [docs](https://docs.pinghome.io/customer-account-management/account-settings/delete-personal-notification-channel/) |
| [Delete Ruleset](actions/delete-ruleset.md) | `DELETE /incident-cmd/v1/ruleset/:id` | [docs](https://docs.pinghome.io/incident-management/ruleset-management-and-event-handling/delete-ruleset/) |
| [Delete Single Heartbeat Monitor](actions/delete-single-heartbeat-monitor.md) | `DELETE /resource-cmd/v1/heartbeat/:id` | [docs](https://docs.pinghome.io/monitoring/heartbeat-monitoring/delete-single-heartbeat-monitor/) |
| [Delete Statuspage](actions/delete-statuspage.md) | `DELETE /statuspage-cmd/v1/statuspage/:id` | [docs](https://docs.pinghome.io/statuspages/delete-statuspage/) |
| [Delete Statuspage Subscription](actions/delete-statuspage-subscription.md) | `DELETE /statuspage-cmd/v1/subscription/:token` | [docs](https://docs.pinghome.io/statuspages/delete-statuspage-subscription/) |
| [Delete Subscription](actions/delete-subscription.md) | `DELETE /payment-cmd/v1/subscription/:id` | [docs](https://docs.pinghome.io/billing-operations-management/delete-subscription/) |
| [Delete Team](actions/delete-team.md) | `DELETE /customer-cmd/v1/team/:id` | [docs](https://docs.pinghome.io/customer-account-management/team-organization-and-role-setup/delete-team/) |
| [Delete Uptime Monitor](actions/delete-uptime-monitor.md) | `DELETE /resource-cmd/v1/resource/:id` | [docs](https://docs.pinghome.io/monitoring/uptime-monitoring/delete-uptime-monitor/) |
| [Get Account Payment Method Information](actions/get-account-payment-method-information.md) | `GET /payment-query/v1/payment-methods` | [docs](https://docs.pinghome.io/billing-operations-management/get-account-payment-method-information/) |
| [Get Comprehensive Statuspage Details](actions/get-comprehensive-statuspage-details.md) | `GET /statuspage-query/v1/statuspage/:id/unified` | [docs](https://docs.pinghome.io/statuspages/get-comprehensive-statuspage-details/) |
| [Get Customer Profile](actions/get-customer-profile.md) | `GET /customer-query/v1/customer` | [docs](https://docs.pinghome.io/customer-account-management/account-settings/get-customer-profile/) |
| [Get Domain Cname Settings](actions/get-domain-cname-settings.md) | `GET /statuspage-query/v1/domain/:domain/cname` | [docs](https://docs.pinghome.io/statuspages/get-domain-cname-settings/) |
| [Get Organisation Usage](actions/get-organisation-usage.md) | `GET /customer-query/v1/org/usage` | [docs](https://docs.pinghome.io/billing-operations-management/get-organisation-usage/) |
| [Get Plan Limits By Version](actions/get-plan-limits-by-version.md) | `GET https://customer-query.api.pinghome.io/v1/plan/:plan/:version/limits` | [docs](https://docs.pinghome.io/billing-operations-management/get-plan-limits-by-version/) |
| [Get Service Details](actions/get-service-details.md) | `GET /resource-query/v1/team-service/:id` | [docs](https://docs.pinghome.io/customer-account-management/team-organization-and-role-setup/get-service-details/) |
| [Get Specific Heartbeat Information](actions/get-specific-heartbeat-information.md) | `GET /resource-query/v1/heartbeat/:id` | [docs](https://docs.pinghome.io/monitoring/heartbeat-monitoring/get-specific-heartbeat-information/) |
| [Get Specific Uptime Monitor](actions/get-specific-uptime-monitor.md) | `GET /resource-query/v1/resource/:id` | [docs](https://docs.pinghome.io/monitoring/uptime-monitoring/get-specific-uptime-monitor/) |
| [Get Statistics For Statuspage Component](actions/get-statistics-for-statuspage-component.md) | `GET /statuspage-query/v1/component/:id/statistics` | [docs](https://docs.pinghome.io/statuspages/get-statistics-for-statuspage-component/) |
| [Get Statuspage](actions/get-statuspage.md) | `GET /statuspage-query/v1/statuspage/:id` | [docs](https://docs.pinghome.io/statuspages/get-statuspage/) |
| [Get Subscription Payment History](actions/get-subscription-payment-history.md) | `GET /payment-query/v1/subscription/:id/payments` | [docs](https://docs.pinghome.io/billing-operations-management/get-subscription-payment-history/) |
| [Get Subscription Proration Details](actions/get-subscription-proration-details.md) | `GET /payment-query/v1/subscription/:id/proration/:product_id` | [docs](https://docs.pinghome.io/billing-operations-management/get-subscription-proration-details/) |
| [List Customer Schedules](actions/list-customer-schedules.md) | `GET /incident-query/v1/customer/:id/schedule` | [docs](https://docs.pinghome.io/incident-management/incident-schedule-management/get-customer-schedules/) |
| [List Incident Actions](actions/list-incident-actions.md) | `GET /incident-query/v1/incident/:id/actions` | [docs](https://docs.pinghome.io/incident-management/incident-tracking/get-incident-actions/) |
| [List Personal Notification Channels](actions/list-personal-notification-channels.md) | `GET /customer-query/v1/customer/:id/notification-channels` | [docs](https://docs.pinghome.io/customer-account-management/account-settings/get-personal-notification-channels/) |
| [List Ruleset Actions](actions/list-ruleset-actions.md) | `GET /incident-query/v1/ruleset/:id/actions` | [docs](https://docs.pinghome.io/incident-management/ruleset-management-and-event-handling/get-ruleset-actions/) |
| [List Rulesets](actions/list-rulesets.md) | `GET /incident-query/v1/rulesets` | [docs](https://docs.pinghome.io/incident-management/ruleset-management-and-event-handling/get-rulesets/) |
| [List Service Heartbeats](actions/list-service-heartbeats.md) | `GET /resource-query/v1/service/:id/heartbeats` | [docs](https://docs.pinghome.io/monitoring/heartbeat-monitoring/get-service-heartbeats/) |
| [List Statuspage Components](actions/list-statuspage-components.md) | `GET /statuspage-query/v1/statuspage/:id/components` | [docs](https://docs.pinghome.io/statuspages/get-statuspage-components/) |
| [List Statuspage Subscriptions](actions/list-statuspage-subscriptions.md) | `GET /statuspage-query/v1/statuspage/:id/subscriptions` | [docs](https://docs.pinghome.io/statuspages/get-statuspage-subscriptions/) |
| [List Statuspages For Organisation](actions/list-statuspages-for-organisation.md) | `GET /statuspage-query/v1/statuspages` | [docs](https://docs.pinghome.io/statuspages/get-statuspages-for-organisation/) |
| [List Team Incidents](actions/list-team-incidents.md) | `GET /incident-query/v1/team/:id/incidents` | [docs](https://docs.pinghome.io/incident-management/incident-tracking/get-team-incidents/) |
| [List Team Members](actions/list-team-members.md) | `GET /customer-query/v1/team/:id/members` | [docs](https://docs.pinghome.io/customer-account-management/team-organization-and-role-setup/get-team-members/) |
| [List Team Notification Channels](actions/list-team-notification-channels.md) | `GET /customer-query/v1/team/:id/notification-channels` | [docs](https://docs.pinghome.io/customer-account-management/team-organization-and-role-setup/get-team-notification-channels/) |
| [List Teams](actions/list-teams.md) | `GET /customer-query/v1/teams` | [docs](https://docs.pinghome.io/customer-account-management/team-organization-and-role-setup/get-teams/) |
| [List Uptime Monitor Regions](actions/list-uptime-monitor-regions.md) | `GET /resource-query/v1/resource/:id/regions` | [docs](https://docs.pinghome.io/monitoring/uptime-monitoring/get-uptime-monitor-regions/) |
| [List Webhook Events](actions/list-webhook-events.md) | `GET /incident-query/v1/webhook/:id/events` | [docs](https://docs.pinghome.io/incident-management/ruleset-management-and-event-handling/get-webhook-events/) |
| [List Webhooks](actions/list-webhooks.md) | `GET /incident-query/v1/webhooks` | [docs](https://docs.pinghome.io/incident-management/ruleset-management-and-event-handling/get-webhooks/) |
| [Setup Heartbeat Monitor](actions/setup-heartbeat-monitor.md) | `POST /resource-cmd/v1/heartbeat` | [docs](https://docs.pinghome.io/monitoring/heartbeat-monitoring/setup-heartbeat-monitor/) |
| [Update Customer Information](actions/update-customer-information.md) | `PATCH /customer-cmd/v1/customer` | [docs](https://docs.pinghome.io/customer-account-management/account-settings/update-customer-information/) |
| [Update Heartbeat Monitor](actions/update-heartbeat-monitor.md) | `PUT /resource-cmd/v1/heartbeat/:id` | [docs](https://docs.pinghome.io/monitoring/heartbeat-monitoring/update-heartbeat-monitor/) |
| [Update Incident](actions/update-incident.md) | `PUT /incident-cmd/v1/incident/:id` | [docs](https://docs.pinghome.io/incident-management/incident-tracking/update-incident/) |
| [Update Oncall Schedule](actions/update-oncall-schedule.md) | `PUT /incident-cmd/v1/team/:id/schedule` | [docs](https://docs.pinghome.io/incident-management/incident-schedule-management/update-oncall-schedule/) |
| [Update Organisation Plan](actions/update-organisation-plan.md) | `PUT /customer-cmd/v1/organisation/plan` | [docs](https://docs.pinghome.io/billing-operations-management/update-organisation-plan/) |
| [Update Personal Notification Channel](actions/update-personal-notification-channel.md) | `PUT /customer-cmd/v1/customer/:id/notification-channel` | [docs](https://docs.pinghome.io/customer-account-management/account-settings/update-personal-notification-channel/) |
| [Update Personal Notification Channel Status](actions/update-personal-notification-channel-status.md) | `PUT /customer-cmd/v1/customer/:id/notification-channel/enabled` | [docs](https://docs.pinghome.io/customer-account-management/account-settings/update-personal-notification-channel-status/) |
| [Update Ruleset](actions/update-ruleset.md) | `PUT /incident-cmd/v1/ruleset/:id` | [docs](https://docs.pinghome.io/incident-management/ruleset-management-and-event-handling/update-ruleset/) |
| [Update Ruleset Actions](actions/update-ruleset-actions.md) | `PUT /incident-cmd/v1/ruleset/:id/actions` | [docs](https://docs.pinghome.io/incident-management/ruleset-management-and-event-handling/update-ruleset-actions/) |
| [Update Statuspage](actions/update-statuspage.md) | `PUT /statuspage-cmd/v1/statuspage/:id` | [docs](https://docs.pinghome.io/statuspages/update-statuspage/) |
| [Update Statuspage Status](actions/update-statuspage-status.md) | `PUT /statuspage-cmd/v1/statuspage/:id/status` | [docs](https://docs.pinghome.io/statuspages/update-statuspage-status/) |
| [Update Subscription](actions/update-subscription.md) | `PATCH /payment-cmd/v1/subscription/:id` | [docs](https://docs.pinghome.io/billing-operations-management/update-subscription/) |
| [Update Team Member](actions/update-team-member.md) | `PATCH /customer-cmd/v1/team/:id/member/:memberId` | [docs](https://docs.pinghome.io/customer-account-management/team-organization-and-role-setup/update-team-member/) |
| [Update Team Notification Channel](actions/update-team-notification-channel.md) | `PUT /customer-cmd/v1/team/:id/notification-channel` | [docs](https://docs.pinghome.io/customer-account-management/team-organization-and-role-setup/update-team-notification-channel/) |
| [Update Team Notification Channel Status](actions/update-team-notification-channel-status.md) | `PUT /customer-cmd/v1/team/:id/notification-channel/enabled` | [docs](https://docs.pinghome.io/customer-account-management/team-organization-and-role-setup/update-team-notification-channel-status/) |
| [Update Uptime Monitor](actions/update-uptime-monitor.md) | `PUT /resource-cmd/v1/resource/:id` | [docs](https://docs.pinghome.io/monitoring/uptime-monitoring/update-uptime-monitor/) |
| [View Heartbeat Statistics](actions/view-heartbeat-statistics.md) | `GET /statistic-query/v1/heartbeat/:id/statistic` | [docs](https://docs.pinghome.io/monitoring/heartbeat-monitoring/view-heartbeat-statistics/) |
| [View Uptime Monitor Performance Report](actions/view-uptime-monitor-performance-report.md) | `GET /statistic-query/v1/resource/:id/statistic` | [docs](https://docs.pinghome.io/monitoring/uptime-monitoring/view-uptime-monitor-performance-report/) |
| [View Uptime Monitor Response Log History](actions/view-uptime-monitor-response-log-history.md) | `GET /response-manager/v1/resource/:id/responses` | [docs](https://docs.pinghome.io/monitoring/uptime-monitoring/view-uptime-monitor-response-log-history/) |
| [View Uptime Monitor State Change History](actions/view-uptime-monitor-state-change-history.md) | `GET /statistic-query/v1/resource/:id/state-changed-logs` | [docs](https://docs.pinghome.io/monitoring/uptime-monitoring/view-uptime-monitor-state-change-history/) |
