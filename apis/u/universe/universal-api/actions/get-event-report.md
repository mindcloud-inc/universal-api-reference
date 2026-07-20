# Universe: Get Event Report

Retrieves the report preview for a Universe event.

```
GET https://connect.mindcloud.co/v1/universal/universe/latest/actions/get-event-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Universe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/universe/latest/actions/get-event-report?connectionId=$CONNECTION_ID&query=query%20GetEventReport(%24eventId%3A%20ID!)%20%7B%0A%20%20event(id%3A%20%24eventId)%20%7B%0A%20%20%20%20id%0A%20%20%20%20title%0A%20%20%20%20report%20%7B%0A%20%20%20%20%20%20columns%0A%20%20%20%20%20%20preview%0A%20%20%20%20%7D%0A%20%20%7D%0A%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "query GetEventReport($eventId: ID!) {\n  event(id: $eventId) {\n    id\n    title\n    report {\n      columns\n      preview\n    }\n  }\n}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/universe/latest/actions/get-event-report?${params}`, {
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
| `query` | string | yes | Universe GraphQL query document to execute for this action. Default: `query GetEventReport($eventId: ID!) {\n  event(id: $eventId) {\n    id\n    title\n    report {\n      columns\n      preview\n    }\n  }\n}`. |
| `variables` | object | no | Optional GraphQL variables object for the event report query. Default: `{"eventId":"69bc5bb99abe4b003ceea74f"}`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Universe API returns.

## Native endpoint

Through the native Universe API, this operation is `POST /graphql` (base URL `https://www.universe.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-report.md) for the provider-specific parameters and requirements.

