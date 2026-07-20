# <img src="https://images.mindcloud.co/apps/icons/s-ignl4_1774559156685.png" alt="SIGNL4 logo" width="28" height="28"> SIGNL4: Universal API

SIGNL4 is a mobile alerting, incident response, and on-call duty management platform for routing alerts, events, schedules, teams, and user duty workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sIGNL4/latest
- **Category:** Support / Ticketing
- **Actions:** 47
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.signl4.com
- **Vendor API docs:** https://docs.signl4.com/integrations/rest-api/rest-api.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Teams](actions/list-teams.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (47)

### Alert

| Action | Method | Description |
| --- | --- | --- |
| [Acknowledge Alert](actions/acknowledge-alert.md) | PUT | Updates an alert as acknowledged in SIGNL4. |
| [Close Alert](actions/close-alert.md) | PUT | Updates an alert as closed in SIGNL4. |
| [Get Alert](actions/get-alert.md) | GET | Retrieves an alert from SIGNL4 by ID. |
| [Get Alert Details](actions/get-alert-details.md) | GET | Retrieves alert details from SIGNL4. |
| [List Alerts](actions/list-alerts.md) | GET | Retrieves alerts from SIGNL4. |
| [Trigger Alert](actions/trigger-alert.md) | POST | Creates an alert in SIGNL4. |

### Alert Annotation

| Action | Method | Description |
| --- | --- | --- |
| [Annotate Alert](actions/annotate-alert.md) | POST | Creates an annotation for an alert in SIGNL4. |

### Alert Distribution

| Action | Method | Description |
| --- | --- | --- |
| [Get Alert Distribution](actions/get-alert-distribution.md) | GET | Retrieves alert distribution details from SIGNL4. |

### Alert Notification

| Action | Method | Description |
| --- | --- | --- |
| [Get Alert Notifications](actions/get-alert-notifications.md) | GET | Retrieves alert notifications from SIGNL4. |

### Alert Parameter

| Action | Method | Description |
| --- | --- | --- |
| [Get Alert Parameters](actions/get-alert-parameters.md) | GET | Retrieves alert parameters from SIGNL4. |

### Alert Summary

| Action | Method | Description |
| --- | --- | --- |
| [Create Alert Summary](actions/create-alert-summary.md) | POST | Creates an alert summary in SIGNL4. |
| [Get Alert Summary](actions/get-alert-summary.md) | GET | Retrieves an alert summary from SIGNL4. |

### Alert Timeline Entry

| Action | Method | Description |
| --- | --- | --- |
| [Get Alert Timeline](actions/get-alert-timeline.md) | GET | Retrieves an alert timeline from SIGNL4. |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Create Category](actions/create-category.md) | POST | Creates a category in SIGNL4. |
| [Delete Category](actions/delete-category.md) | DELETE | Deletes a category from SIGNL4. |
| [List Team Categories](actions/list-team-categories.md) | GET | Retrieves categories for a team from SIGNL4. |
| [Update Category](actions/update-category.md) | PUT | Updates a category in SIGNL4. |

### Category Metric

| Action | Method | Description |
| --- | --- | --- |
| [Get Category Metrics](actions/get-category-metrics.md) | GET | Retrieves category metrics from SIGNL4. |

### Duty

| Action | Method | Description |
| --- | --- | --- |
| [Get Duty Summary](actions/get-duty-summary.md) | GET | Retrieves duty summaries from SIGNL4. |
| [Punch User In](actions/punch-user-in.md) | PUT | Updates a user's duty status to on-duty in SIGNL4. |
| [Punch User Out](actions/punch-user-out.md) | PUT | Updates a user's duty status to off-duty in SIGNL4. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST | Creates an event in SIGNL4. |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from SIGNL4 by ID. |
| [List Events](actions/list-events.md) | GET | Retrieves events from SIGNL4. |

### Event Overview

| Action | Method | Description |
| --- | --- | --- |
| [Get Event Overview](actions/get-event-overview.md) | GET | Retrieves an event overview from SIGNL4. |

### Event Parameter

| Action | Method | Description |
| --- | --- | --- |
| [Get Event Parameters](actions/get-event-parameters.md) | GET | Retrieves event parameters from SIGNL4. |

### Event Source

| Action | Method | Description |
| --- | --- | --- |
| [Create Event Source](actions/create-event-source.md) | POST | Creates an event source in SIGNL4. |
| [Delete Event Source](actions/delete-event-source.md) | DELETE | Deletes an event source from SIGNL4. |
| [Get Event Source](actions/get-event-source.md) | GET | Retrieves an event source from SIGNL4 by ID. |
| [List Event Sources](actions/list-event-sources.md) | GET | Retrieves event sources from SIGNL4. |
| [Update Event Source](actions/update-event-source.md) | PUT | Updates an event source in SIGNL4. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [List Team Event Sources](actions/list-team-event-sources.md) | GET | Retrieves event sources for a team from SIGNL4. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Alert Report](actions/get-alert-report.md) | GET | Retrieves an alert report from SIGNL4. |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Get Subscription](actions/get-subscription.md) | GET | Retrieves a subscription from SIGNL4 by ID. |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves subscriptions from SIGNL4. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Get Team](actions/get-team.md) | GET | Retrieves a team from SIGNL4 by ID. |
| [List Teams](actions/list-teams.md) | GET | Retrieves teams from SIGNL4. |

### Team Membership

| Action | Method | Description |
| --- | --- | --- |
| [Add User To Team](actions/add-user-to-team.md) | POST | Creates a team membership in SIGNL4. |
| [List Team Memberships](actions/list-team-memberships.md) | GET | Retrieves team memberships from SIGNL4. |
| [Remove Team Membership](actions/remove-team-membership.md) | DELETE | Deletes a team membership from SIGNL4. |
| [Update Team Membership](actions/update-team-membership.md) | PUT | Updates a team membership in SIGNL4. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [Get Team Alert Settings](actions/get-team-alert-settings.md) | GET | Retrieves alert settings for a team from SIGNL4. |
| [Get Team Setup Progress](actions/get-team-setup-progress.md) | GET | Retrieves team setup progress from SIGNL4. |
| [List Subscription Teams](actions/list-subscription-teams.md) | GET | Retrieves teams for a subscription from SIGNL4. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user from SIGNL4 by ID. |
| [List Users](actions/list-users.md) | GET | Retrieves users from SIGNL4. |

### User Duty Status

| Action | Method | Description |
| --- | --- | --- |
| [Get User Duty Status](actions/get-user-duty-status.md) | GET | Retrieves a user's duty status from SIGNL4. |

