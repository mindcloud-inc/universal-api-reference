# Flow App: Native API Reference

A consolidated summary of Flow App's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://support.flowapp.com/support/solutions/articles/12000076814-flow-api-0-0-4
- **API base URL:** `https://prod.flowapp.com/api/v1`

## Authentication

### API Key

Authenticate requests with the Flow account API key exposed in the dashboard Account page.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
api-secret: <apiKey>
```

[Official authentication documentation](https://support.flowapp.com/support/solutions/articles/12000076814-flow-api-0-0-4)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | `POST /event` | [docs](https://support.flowapp.com/support/solutions/articles/12000076814-flow-api-0-0-4) |
| [Create Registrant](actions/create-registrant.md) | `POST /registrants` | [docs](https://support.flowapp.com/support/solutions/articles/12000076814-flow-api-0-0-4) |
| [Get Attendee Chat CSV](actions/get-attendee-chat-csv.md) | `GET /reports/events/sessions/csv/attendeeChat/:sessionToken` | [docs](https://support.flowapp.com/support/solutions/articles/12000076814-flow-api-0-0-4) |
| [Get Event](actions/get-event.md) | `GET /events/sessions/:sessionToken` | [docs](https://support.flowapp.com/support/solutions/articles/12000076814-flow-api-0-0-4) |
| [Get Event Summary CSV](actions/get-event-summary-csv.md) | `GET /reports/events/sessions/csv/summary/:sessionToken` | [docs](https://support.flowapp.com/support/solutions/articles/12000076814-flow-api-0-0-4) |
| [Get Operator Chat CSV](actions/get-operator-chat-csv.md) | `GET /reports/events/sessions/csv/operatorChat/:sessionToken` | [docs](https://support.flowapp.com/support/solutions/articles/12000076814-flow-api-0-0-4) |
| [Get Registrants CSV](actions/get-registrants-csv.md) | `GET /reports/events/sessions/csv/registrants/:sessionToken` | [docs](https://support.flowapp.com/support/solutions/articles/12000076814-flow-api-0-0-4) |
| [Get Survey Responses CSV](actions/get-survey-responses-csv.md) | `GET /reports/events/sessions/csv/surveyDetail/:sessionToken/:surveyId` | [docs](https://support.flowapp.com/support/solutions/articles/12000076814-flow-api-0-0-4) |
| [List Event Surveys](actions/list-event-surveys.md) | `GET /reports/events/sessions/surveys/:sessionToken` | [docs](https://support.flowapp.com/support/solutions/articles/12000076814-flow-api-0-0-4) |
| [List Events](actions/list-events.md) | `GET /events/sessions` | [docs](https://support.flowapp.com/support/solutions/articles/12000076814-flow-api-0-0-4) |
| [List Operators](actions/list-operators.md) | `GET /users` | [docs](https://support.flowapp.com/support/solutions/articles/12000076814-flow-api-0-0-4) |
| [List Registrants](actions/list-registrants.md) | `GET /reports/events/sessions/registrants/:sessionToken` | [docs](https://support.flowapp.com/support/solutions/articles/12000076814-flow-api-0-0-4) |
