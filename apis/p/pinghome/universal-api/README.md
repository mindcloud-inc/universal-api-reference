# <img src="https://images.mindcloud.co/apps/icons/pinghome_1774900558922.png" alt="Pinghome logo" width="28" height="28"> Pinghome: Universal API

Pinghome is an uptime monitoring and incident management platform for websites, APIs, servers, status pages, and on-call operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pinghome/latest
- **Category:** IT Operations / Observability
- **Actions:** 72
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.pinghome.io
- **Vendor API docs:** https://docs.pinghome.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Customer Profile](actions/get-customer-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/get-customer-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (72)

### Channels

| Action | Method | Description |
| --- | --- | --- |
| [Delete Personal Notification Channel](actions/delete-personal-notification-channel.md) | DELETE | Deletes an existing personal notification channel from Pinghome. |
| [List Personal Notification Channels](actions/list-personal-notification-channels.md) | GET | Retrieves personal notification channels from Pinghome. |
| [List Team Notification Channels](actions/list-team-notification-channels.md) | GET | Retrieves team notification channels from Pinghome. |
| [Update Personal Notification Channel](actions/update-personal-notification-channel.md) | PUT | Updates an existing personal notification channel in Pinghome. |
| [Update Personal Notification Channel Status](actions/update-personal-notification-channel-status.md) | PUT | Updates personal notification channel status in Pinghome. |
| [Update Team Notification Channel](actions/update-team-notification-channel.md) | PUT | Updates an existing team notification channel in Pinghome. |
| [Update Team Notification Channel Status](actions/update-team-notification-channel-status.md) | PUT | Updates team notification channel status in Pinghome. |

### Component

| Action | Method | Description |
| --- | --- | --- |
| [List Statuspage Components](actions/list-statuspage-components.md) | GET | Retrieves statuspage components from Pinghome. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer Profile](actions/get-customer-profile.md) | GET | Retrieves customer profile information from Pinghome. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Update Customer Information](actions/update-customer-information.md) | PUT | Updates existing customer information in Pinghome. |

### Domain Cname Setting

| Action | Method | Description |
| --- | --- | --- |
| [Get Domain Cname Settings](actions/get-domain-cname-settings.md) | GET | Retrieves domain CNAME settings from Pinghome. |

### Incident

| Action | Method | Description |
| --- | --- | --- |
| [Create Incident](actions/create-incident.md) | POST | Creates a new incident in Pinghome. |
| [List Team Incidents](actions/list-team-incidents.md) | GET | Retrieves team incidents from Pinghome. |
| [Update Incident](actions/update-incident.md) | PUT | Updates an existing incident in Pinghome. |

### Incident Action

| Action | Method | Description |
| --- | --- | --- |
| [List Incident Actions](actions/list-incident-actions.md) | GET | Retrieves incident actions from Pinghome. |

### Organisation Plan

| Action | Method | Description |
| --- | --- | --- |
| [Update Organisation Plan](actions/update-organisation-plan.md) | PUT | Updates the organisation plan in Pinghome. |

### Organisation Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Organisation Usage](actions/get-organisation-usage.md) | GET | Retrieves organisation usage from Pinghome. |

### Payment Method

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Payment Method Information](actions/get-account-payment-method-information.md) | GET | Retrieves account payment method information from Pinghome. |

### Personal Notification Channel

| Action | Method | Description |
| --- | --- | --- |
| [Create Personal Notification Channel](actions/create-personal-notification-channel.md) | POST | Creates a new personal notification channel in Pinghome. |

### Plan Limit

| Action | Method | Description |
| --- | --- | --- |
| [Get Plan Limits By Version](actions/get-plan-limits-by-version.md) | GET | Retrieves plan limits from Pinghome by version. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [View Heartbeat Statistics](actions/view-heartbeat-statistics.md) | GET | Retrieves heartbeat statistics from Pinghome. |
| [View Uptime Monitor Performance Report](actions/view-uptime-monitor-performance-report.md) | GET | Retrieves an uptime monitor performance report from Pinghome. |
| [View Uptime Monitor Response Log History](actions/view-uptime-monitor-response-log-history.md) | GET | Retrieves uptime monitor response log history from Pinghome. |
| [View Uptime Monitor State Change History](actions/view-uptime-monitor-state-change-history.md) | GET | Retrieves uptime monitor state change history from Pinghome. |

### Ruleset

| Action | Method | Description |
| --- | --- | --- |
| [Create Ruleset](actions/create-ruleset.md) | POST | Creates a new ruleset in Pinghome. |
| [Delete Ruleset](actions/delete-ruleset.md) | DELETE | Deletes an existing ruleset from Pinghome. |
| [List Rulesets](actions/list-rulesets.md) | GET | Retrieves rulesets from Pinghome. |
| [Update Ruleset](actions/update-ruleset.md) | PUT | Updates an existing ruleset in Pinghome. |

### Ruleset Action

| Action | Method | Description |
| --- | --- | --- |
| [List Ruleset Actions](actions/list-ruleset-actions.md) | GET | Retrieves ruleset actions from Pinghome. |
| [Update Ruleset Actions](actions/update-ruleset-actions.md) | PUT | Updates existing ruleset actions in Pinghome. |

### Schedule

| Action | Method | Description |
| --- | --- | --- |
| [Create Oncall Schedule](actions/create-oncall-schedule.md) | POST | Creates a new on-call schedule in Pinghome. |
| [Delete Oncall Schedule](actions/delete-oncall-schedule.md) | DELETE | Deletes an existing on-call schedule from Pinghome. |
| [List Customer Schedules](actions/list-customer-schedules.md) | GET | Retrieves customer schedules from Pinghome. |
| [Update Oncall Schedule](actions/update-oncall-schedule.md) | PUT | Updates an existing on-call schedule in Pinghome. |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [Create Service](actions/create-service.md) | POST | Creates a new service in Pinghome. |
| [Get Service Details](actions/get-service-details.md) | GET | Retrieves service details from Pinghome. |

### Service Health

| Action | Method | Description |
| --- | --- | --- |
| [Check Service Health Status](actions/check-service-health-status.md) | GET | Retrieves service health status from Pinghome. |

### Statuspage

| Action | Method | Description |
| --- | --- | --- |
| [Create Statuspage](actions/create-statuspage.md) | POST | Creates a new statuspage in Pinghome. |
| [Delete Statuspage](actions/delete-statuspage.md) | DELETE | Deletes an existing statuspage from Pinghome. |
| [Get Comprehensive Statuspage Details](actions/get-comprehensive-statuspage-details.md) | GET | Retrieves comprehensive statuspage details from Pinghome. |
| [Get Statuspage](actions/get-statuspage.md) | GET | Retrieves a statuspage from Pinghome. |
| [List Statuspages For Organisation](actions/list-statuspages-for-organisation.md) | GET | Retrieves organisation statuspages from Pinghome. |
| [Update Statuspage](actions/update-statuspage.md) | PUT | Updates an existing statuspage in Pinghome. |
| [Update Statuspage Status](actions/update-statuspage-status.md) | PUT | Updates statuspage status in Pinghome. |

### Statuspage Component Statistic

| Action | Method | Description |
| --- | --- | --- |
| [Get Statistics For Statuspage Component](actions/get-statistics-for-statuspage-component.md) | GET | Retrieves statuspage component statistics from Pinghome. |

### Statuspage Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscription For Statuspages](actions/create-subscription-for-statuspages.md) | POST | Creates a new statuspage subscription in Pinghome. |
| [Delete Statuspage Subscription](actions/delete-statuspage-subscription.md) | DELETE | Deletes an existing statuspage subscription from Pinghome. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Delete Subscription](actions/delete-subscription.md) | DELETE | Deletes an existing subscription from Pinghome. |
| [List Statuspage Subscriptions](actions/list-statuspage-subscriptions.md) | GET | Retrieves statuspage subscriptions from Pinghome. |
| [Update Subscription](actions/update-subscription.md) | PUT | Updates an existing subscription in Pinghome. |

### Subscription Payment

| Action | Method | Description |
| --- | --- | --- |
| [Get Subscription Payment History](actions/get-subscription-payment-history.md) | GET | Retrieves subscription payment history from Pinghome. |

### Subscription Proration

| Action | Method | Description |
| --- | --- | --- |
| [Get Subscription Proration Details](actions/get-subscription-proration-details.md) | GET | Retrieves subscription proration details from Pinghome. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Create Team](actions/create-team.md) | POST | Creates a new team in Pinghome. |

### Team Notification Channel

| Action | Method | Description |
| --- | --- | --- |
| [Create Team Notification Channel](actions/create-team-notification-channel.md) | POST | Creates a new team notification channel in Pinghome. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [Delete Team](actions/delete-team.md) | DELETE | Deletes an existing team from Pinghome. |
| [List Teams](actions/list-teams.md) | GET | Retrieves teams from Pinghome. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Change Uptime Monitor Status](actions/change-uptime-monitor-status.md) | PUT | Updates uptime monitor status in Pinghome. |
| [Delete Single Heartbeat Monitor](actions/delete-single-heartbeat-monitor.md) | DELETE | Deletes an existing heartbeat monitor from Pinghome. |
| [Delete Uptime Monitor](actions/delete-uptime-monitor.md) | DELETE | Deletes an existing uptime monitor from Pinghome. |
| [Get Specific Heartbeat Information](actions/get-specific-heartbeat-information.md) | GET | Retrieves specific heartbeat information from Pinghome. |
| [Get Specific Uptime Monitor](actions/get-specific-uptime-monitor.md) | GET | Retrieves a specific uptime monitor from Pinghome. |
| [List Service Heartbeats](actions/list-service-heartbeats.md) | GET | Retrieves service heartbeats from Pinghome. |
| [List Uptime Monitor Regions](actions/list-uptime-monitor-regions.md) | GET | Retrieves uptime monitor regions from Pinghome. |
| [Setup Heartbeat Monitor](actions/setup-heartbeat-monitor.md) | POST | Creates a new heartbeat monitor in Pinghome. |
| [Update Heartbeat Monitor](actions/update-heartbeat-monitor.md) | PUT | Updates an existing heartbeat monitor in Pinghome. |
| [Update Uptime Monitor](actions/update-uptime-monitor.md) | PUT | Updates an existing uptime monitor in Pinghome. |

### Uptime Monitor

| Action | Method | Description |
| --- | --- | --- |
| [Create Uptime Monitor](actions/create-uptime-monitor.md) | POST | Creates a new uptime monitor in Pinghome. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Team Members](actions/list-team-members.md) | GET | Retrieves team members from Pinghome. |
| [Update Team Member](actions/update-team-member.md) | PUT | Updates an existing team member in Pinghome. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Pinghome. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Pinghome. |

### Webhook Event

| Action | Method | Description |
| --- | --- | --- |
| [List Webhook Events](actions/list-webhook-events.md) | GET | Retrieves webhook events from Pinghome. |

