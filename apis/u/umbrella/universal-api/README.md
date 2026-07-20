# <img src="https://images.mindcloud.co/apps/icons/images-34_1774903488733.png" alt="Umbrella logo" width="28" height="28"> Umbrella: Universal API

Cisco Umbrella provides cloud-delivered DNS-layer security and exposes APIs for managing users, roles, alert rules, alerts, integrations, and organization lookups through the Umbrella and Cisco SSE admin APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/umbrella/latest
- **Actions:** 35
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.cisco.com/site/us/en/products/security/umbrella/index.html
- **Vendor API docs:** https://developer.cisco.com/docs/cloud-security/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Roles](actions/list-roles.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/list-roles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (35)

### Alert

| Action | Method | Description |
| --- | --- | --- |
| [Count Active Alerts](actions/count-active-alerts.md) | GET | Retrieves the count of active alerts from Umbrella. |
| [List Active Alerts](actions/list-active-alerts.md) | GET | Retrieves active alert records from Umbrella. |
| [List Active High Severity Alerts](actions/list-active-high-severity-alerts.md) | GET | Retrieves active high-severity alerts from Umbrella. |
| [List Alerts](actions/list-alerts.md) | GET | Retrieves alert records from your Umbrella organization. |
| [List Alerts With Context](actions/list-alerts-with-context.md) | GET | Retrieves alerts with context metadata from Umbrella. |
| [List Archived Alerts](actions/list-archived-alerts.md) | GET | Retrieves archived alert records from Umbrella. |
| [List Dismissed Alerts](actions/list-dismissed-alerts.md) | GET | Retrieves dismissed alert records from Umbrella. |
| [List High Severity Alerts](actions/list-high-severity-alerts.md) | GET | Retrieves high-severity alert records from Umbrella. |
| [List Info Alerts](actions/list-info-alerts.md) | GET | Retrieves informational alert records from Umbrella. |
| [List Low Severity Alerts](actions/list-low-severity-alerts.md) | GET | Retrieves low-severity alert records from Umbrella. |
| [List Medium Severity Alerts](actions/list-medium-severity-alerts.md) | GET | Retrieves medium-severity alert records from Umbrella. |
| [List Resolved Alerts](actions/list-resolved-alerts.md) | GET | Retrieves resolved alert records from Umbrella. |

### Alerts

| Action | Method | Description |
| --- | --- | --- |
| [Create Alert Rule](actions/create-alert-rule.md) | POST | Creates a new alert rule in Umbrella. |
| [Delete Alert Rules](actions/delete-alert-rules.md) | DELETE | Deletes existing alert rules from Umbrella. |
| [Get Alert Rule](actions/get-alert-rule.md) | GET | Retrieves an alert rule from Umbrella. |
| [List Alert Rules](actions/list-alert-rules.md) | GET | Retrieves alert rule definitions from Umbrella. |
| [Update Alert Rule](actions/update-alert-rule.md) | PUT | Updates an existing alert rule in Umbrella. |

### Integration

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Integration](actions/create-webhook-integration.md) | POST | Creates a new webhook integration in Umbrella. |
| [Delete Integration](actions/delete-integration.md) | DELETE | Deletes an existing integration from Umbrella. |
| [Get Integration](actions/get-integration.md) | GET | Retrieves integration details from your Umbrella organization. |
| [List Active Integrations](actions/list-active-integrations.md) | GET | Retrieves active integration records from Umbrella. |
| [List Chrome Enterprise Integrations](actions/list-chrome-enterprise-integrations.md) | GET | Retrieves Chrome Enterprise integrations from Umbrella. |
| [List Created Integrations](actions/list-created-integrations.md) | GET | Retrieves integrations in created status from Umbrella. |
| [List Inactive Integrations](actions/list-inactive-integrations.md) | GET | Retrieves inactive integration records from Umbrella. |
| [List Integrations](actions/list-integrations.md) | GET | Retrieves integration records from your Umbrella organization. |
| [List Intune Integrations](actions/list-intune-integrations.md) | GET | Retrieves Intune integration records from Umbrella. |
| [List Jamf Integrations](actions/list-jamf-integrations.md) | GET | Retrieves Jamf integration records from Umbrella. |
| [List Webhook Integrations](actions/list-webhook-integrations.md) | GET | Retrieves webhook integration records from Umbrella. |
| [Update Integration](actions/update-integration.md) | PUT | Updates an existing integration in Umbrella. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [List Organizations by Email](actions/list-organizations-by-email.md) | GET | Finds provider organizations in Umbrella by member email. |

### Role

| Action | Method | Description |
| --- | --- | --- |
| [List Roles](actions/list-roles.md) | GET | Retrieves user role definitions from Umbrella. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in Umbrella. |
| [Delete User](actions/delete-user.md) | DELETE | Deletes an existing user from Umbrella. |
| [Get User](actions/get-user.md) | GET | Retrieves user account details from Umbrella. |
| [List Users](actions/list-users.md) | GET | Retrieves user accounts from your Umbrella organization. |

