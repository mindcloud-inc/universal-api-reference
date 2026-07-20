# <img src="https://images.mindcloud.co/apps/icons/call-tracking-metrics_1773750579693.png" alt="CallTrackingMetrics logo" width="28" height="28"> CallTrackingMetrics: Universal API

Track calls, manage routing, and analyze customer conversations

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/callTrackingMetrics/latest
- **Category:** Marketing
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://calltrackingmetrics.com
- **Vendor API docs:** https://www.postman.com/ctm-8695/calltrackingmetrics-s-public-workspace/documentation/0ygaqwq/ctm-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Active Account IDs And Names](actions/list-active-account-ids-and-names.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/list-active-account-ids-and-names?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves all available accounts from CallTrackingMetrics. |
| [List Active Account IDs And Names](actions/list-active-account-ids-and-names.md) | GET | Retrieves active account IDs and names from CallTrackingMetrics. |

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [List Activities](actions/list-activities.md) | GET | Retrieves account activity records from CallTrackingMetrics. |

### Agency

| Action | Method | Description |
| --- | --- | --- |
| [Get Agency Information](actions/get-agency-information.md) | GET | Retrieves agency information details from CallTrackingMetrics. |

### Agent Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Agent Events](actions/get-agent-events.md) | GET | Retrieves agent event records from CallTrackingMetrics. |

### Call Setting

| Action | Method | Description |
| --- | --- | --- |
| [Get Call Setting Details](actions/get-call-setting-details.md) | GET | Retrieves call setting details from CallTrackingMetrics. |
| [List Call Settings](actions/list-call-settings.md) | GET | Retrieves call settings for an account from CallTrackingMetrics. |
| [Set Default Call Setting](actions/set-default-call-setting.md) | PUT | Sets a default call setting in CallTrackingMetrics. |
| [Update Call Setting](actions/update-call-setting.md) | PUT | Updates an existing call setting in CallTrackingMetrics. |

### Lookup Result

| Action | Method | Description |
| --- | --- | --- |
| [Lookup Objects](actions/lookup-objects.md) | GET | Retrieves lookup objects for an account from CallTrackingMetrics. |

### Number

| Action | Method | Description |
| --- | --- | --- |
| [List Call Setting Number Assignments](actions/list-call-setting-number-assignments.md) | GET | Retrieves call setting number assignments from CallTrackingMetrics. |

### Tracking Source

| Action | Method | Description |
| --- | --- | --- |
| [Create Tracking Source](actions/create-tracking-source.md) | POST | Creates a new tracking source in CallTrackingMetrics. |
| [Delete Tracking Source](actions/delete-tracking-source.md) | DELETE | Deletes an existing tracking source from CallTrackingMetrics. |
| [Get Tracking Source Details](actions/get-tracking-source-details.md) | GET | Retrieves tracking source details from CallTrackingMetrics. |
| [List Tracking Sources](actions/list-tracking-sources.md) | GET | Retrieves tracking sources for an account from CallTrackingMetrics. |
| [Update Tracking Source](actions/update-tracking-source.md) | PUT | Updates an existing tracking source in CallTrackingMetrics. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Details](actions/get-user-details.md) | GET | Retrieves detailed user information from CallTrackingMetrics. |
| [List Users](actions/list-users.md) | GET | Retrieves users for an account from CallTrackingMetrics. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in CallTrackingMetrics. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from CallTrackingMetrics. |
| [Get Webhook Details](actions/get-webhook-details.md) | GET | Retrieves detailed webhook information from CallTrackingMetrics. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks for an account from CallTrackingMetrics. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in CallTrackingMetrics. |

