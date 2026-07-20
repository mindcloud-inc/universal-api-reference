# Universe: List Calendar Widgets

Retrieves calendar widgets for a Universe host.

```
GET https://connect.mindcloud.co/v1/universal/universe/latest/actions/list-calendar-widgets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Universe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/universe/latest/actions/list-calendar-widgets?connectionId=$CONNECTION_ID&query=query%20GetCalendarWidgets(%24hostId%3A%20ID!%2C%20%24startingDate%3A%20String!)%20%7B%0A%20%20calendarWidgets(hostId%3A%20%24hostId%2C%20startingDate%3A%20%24startingDate)%20%7B%0A%20%20%20%20id%0A%20%20%20%20title%0A%20%20%20%20hostId%0A%20%20%20%20timedEntry%0A%20%20%20%20soldOut%0A%20%20%20%20timezone%0A%20%20%20%20transactionCurrency%0A%20%20%7D%0A%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "query GetCalendarWidgets($hostId: ID!, $startingDate: String!) {\n  calendarWidgets(hostId: $hostId, startingDate: $startingDate) {\n    id\n    title\n    hostId\n    timedEntry\n    soldOut\n    timezone\n    transactionCurrency\n  }\n}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/universe/latest/actions/list-calendar-widgets?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | yes | Universe GraphQL query document to execute for this action. Default: `query GetCalendarWidgets($hostId: ID!, $startingDate: String!) {\n  calendarWidgets(hostId: $hostId, startingDate: $startingDate) {\n    id\n    title\n    hostId\n    timedEntry\n    soldOut\n    timezone\n    transactionCurrency\n  }\n}`. |
| `variables` | object | no | Optional GraphQL variables object for the calendar widgets query. Default: `{"hostId":"69bc5b60b86a1d003cef1424","startingDate":"2026-03-19"}`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Universe API returns.

## Native endpoint

Through the native Universe API, this operation is `POST /graphql` (base URL `https://www.universe.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-calendar-widgets.md) for the provider-specific parameters and requirements.

