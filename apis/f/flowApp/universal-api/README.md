# <img src="https://images.mindcloud.co/apps/icons/flow-app_1774905531973.png" alt="Flow App logo" width="28" height="28"> Flow App: Universal API

Webinar platform for managing Flow events, registrants, operators, surveys, and event reports via the official Flow REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/flowApp/latest
- **Category:** Marketing
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.flowapp.com
- **Vendor API docs:** https://support.flowapp.com/support/solutions/articles/12000076814-flow-api-0-0-4

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Operators](actions/list-operators.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flowApp/latest/actions/list-operators?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Event Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Attendee Chat CSV](actions/get-attendee-chat-csv.md) | GET |  |
| [Get Event Summary CSV](actions/get-event-summary-csv.md) | GET |  |
| [Get Operator Chat CSV](actions/get-operator-chat-csv.md) | GET |  |
| [Get Registrants CSV](actions/get-registrants-csv.md) | GET |  |

### Event Session

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST |  |
| [Get Event](actions/get-event.md) | GET |  |
| [List Events](actions/list-events.md) | GET |  |

### Operator

| Action | Method | Description |
| --- | --- | --- |
| [List Operators](actions/list-operators.md) | GET |  |

### Registrant

| Action | Method | Description |
| --- | --- | --- |
| [Create Registrant](actions/create-registrant.md) | POST |  |
| [List Registrants](actions/list-registrants.md) | GET |  |

### Survey

| Action | Method | Description |
| --- | --- | --- |
| [List Event Surveys](actions/list-event-surveys.md) | GET |  |

### Survey Response Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Survey Responses CSV](actions/get-survey-responses-csv.md) | GET |  |

