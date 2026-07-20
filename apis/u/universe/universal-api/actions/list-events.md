# Universe: List Events

Retrieves events for a specified Universe host.

```
GET https://connect.mindcloud.co/v1/universal/universe/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Universe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/universe/latest/actions/list-events?connectionId=$CONNECTION_ID&query=query%20ListEvents(%24hostId%3A%20ID!)%20%7B%0A%20%20host(id%3A%20%24hostId)%20%7B%0A%20%20%20%20id%0A%20%20%20%20name%0A%20%20%20%20events%20%7B%0A%20%20%20%20%20%20nodes%20%7B%0A%20%20%20%20%20%20%20%20id%0A%20%20%20%20%20%20%20%20title%0A%20%20%20%20%20%20%20%20slug%0A%20%20%20%20%20%20%20%20state%0A%20%20%20%20%20%20%20%20url%0A%20%20%20%20%20%20%20%20updatedAt%0A%20%20%20%20%20%20%7D%0A%20%20%20%20%7D%0A%20%20%7D%0A%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "query ListEvents($hostId: ID!) {\n  host(id: $hostId) {\n    id\n    name\n    events {\n      nodes {\n        id\n        title\n        slug\n        state\n        url\n        updatedAt\n      }\n    }\n  }\n}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/universe/latest/actions/list-events?${params}`, {
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
| `query` | string | yes | Universe GraphQL query or mutation document to execute. The default is an events listing example for this action. Default: `query ListEvents($hostId: ID!) {\n  host(id: $hostId) {\n    id\n    name\n    events {\n      nodes {\n        id\n        title\n        slug\n        state\n        url\n        updatedAt\n      }\n    }\n  }\n}`. |
| `variables` | object | no | Optional GraphQL variables as a JSON object string for the default events query. Default: `{"hostId":"HOST_ID"}`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Universe API returns.

## Native endpoint

Through the native Universe API, this operation is `POST /graphql` (base URL `https://www.universe.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

