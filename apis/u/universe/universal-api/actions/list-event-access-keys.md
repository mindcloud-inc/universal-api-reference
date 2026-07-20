# Universe: List Event Access Keys

Retrieves access keys for a specific Universe event.

```
GET https://connect.mindcloud.co/v1/universal/universe/latest/actions/list-event-access-keys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Universe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/universe/latest/actions/list-event-access-keys?connectionId=$CONNECTION_ID&query=query%20ListEventAccessKeys(%24eventId%3A%20ID!%2C%20%24searchQuery%3A%20String)%20%7B%0A%20%20event(id%3A%20%24eventId)%20%7B%0A%20%20%20%20id%0A%20%20%20%20title%0A%20%20%20%20accessKeys(searchQuery%3A%20%24searchQuery)%20%7B%0A%20%20%20%20%20%20nodes%20%7B%0A%20%20%20%20%20%20%20%20id%0A%20%20%20%20%20%20%20%20key%0A%20%20%20%20%20%20%20%20state%0A%20%20%20%20%20%20%20%20quantity%0A%20%20%20%20%20%20%7D%0A%20%20%20%20%7D%0A%20%20%7D%0A%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "query ListEventAccessKeys($eventId: ID!, $searchQuery: String) {\n  event(id: $eventId) {\n    id\n    title\n    accessKeys(searchQuery: $searchQuery) {\n      nodes {\n        id\n        key\n        state\n        quantity\n      }\n    }\n  }\n}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/universe/latest/actions/list-event-access-keys?${params}`, {
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
| `query` | string | yes | Universe GraphQL query or mutation document to execute. The default is an event access-key example for this action. Default: `query ListEventAccessKeys($eventId: ID!, $searchQuery: String) {\n  event(id: $eventId) {\n    id\n    title\n    accessKeys(searchQuery: $searchQuery) {\n      nodes {\n        id\n        key\n        state\n        quantity\n      }\n    }\n  }\n}`. |
| `variables` | object | no | Optional GraphQL variables as a JSON object string for the default access-key query. Default: `{"eventId":"EVENT_ID","searchQuery":""}`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Universe API returns.

## Native endpoint

Through the native Universe API, this operation is `POST /graphql` (base URL `https://www.universe.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-event-access-keys.md) for the provider-specific parameters and requirements.

