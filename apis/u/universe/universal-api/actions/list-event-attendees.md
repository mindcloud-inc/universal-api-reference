# Universe: List Event Attendees

Retrieves attendees for a specific Universe event.

```
GET https://connect.mindcloud.co/v1/universal/universe/latest/actions/list-event-attendees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Universe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/universe/latest/actions/list-event-attendees?connectionId=$CONNECTION_ID&query=query%20ListEventAttendees(%24eventId%3A%20ID!)%20%7B%0A%20%20event(id%3A%20%24eventId)%20%7B%0A%20%20%20%20id%0A%20%20%20%20title%0A%20%20%20%20attendees%20%7B%0A%20%20%20%20%20%20nodes%20%7B%0A%20%20%20%20%20%20%20%20id%0A%20%20%20%20%20%20%20%20firstName%0A%20%20%20%20%20%20%20%20lastName%0A%20%20%20%20%20%20%20%20email%0A%20%20%20%20%20%20%20%20token%0A%20%20%20%20%20%20%20%20state%0A%20%20%20%20%20%20%20%20orderItem%20%7B%0A%20%20%20%20%20%20%20%20%20%20id%0A%20%20%20%20%20%20%20%20%20%20checkInState%0A%20%20%20%20%20%20%20%20%20%20qrCode%0A%20%20%20%20%20%20%20%20%7D%0A%20%20%20%20%20%20%7D%0A%20%20%20%20%7D%0A%20%20%7D%0A%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "query ListEventAttendees($eventId: ID!) {\n  event(id: $eventId) {\n    id\n    title\n    attendees {\n      nodes {\n        id\n        firstName\n        lastName\n        email\n        token\n        state\n        orderItem {\n          id\n          checkInState\n          qrCode\n        }\n      }\n    }\n  }\n}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/universe/latest/actions/list-event-attendees?${params}`, {
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
| `query` | string | yes | Universe GraphQL query or mutation document to execute. The default is an event attendees example for this action. Default: `query ListEventAttendees($eventId: ID!) {\n  event(id: $eventId) {\n    id\n    title\n    attendees {\n      nodes {\n        id\n        firstName\n        lastName\n        email\n        token\n        state\n        orderItem {\n          id\n          checkInState\n          qrCode\n        }\n      }\n    }\n  }\n}`. |
| `variables` | object | no | Optional GraphQL variables as a JSON object string for the default attendees query. Default: `{"eventId":"EVENT_ID"}`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Universe API returns.

## Native endpoint

Through the native Universe API, this operation is `POST /graphql` (base URL `https://www.universe.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-event-attendees.md) for the provider-specific parameters and requirements.

