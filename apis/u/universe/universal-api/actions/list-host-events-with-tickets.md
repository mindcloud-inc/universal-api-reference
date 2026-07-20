# Universe: List Host Events With Tickets

Retrieves ticketed events for a specified Universe host.

```
GET https://connect.mindcloud.co/v1/universal/universe/latest/actions/list-host-events-with-tickets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Universe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/universe/latest/actions/list-host-events-with-tickets?connectionId=$CONNECTION_ID&query=query%20ListHostEventsWithTickets(%24hostId%3A%20ID!)%20%7B%0A%20%20host(id%3A%20%24hostId)%20%7B%0A%20%20%20%20id%0A%20%20%20%20name%0A%20%20%20%20eventsWithTickets%20%7B%0A%20%20%20%20%20%20nodes%20%7B%0A%20%20%20%20%20%20%20%20id%0A%20%20%20%20%20%20%20%20title%0A%20%20%20%20%20%20%20%20slug%0A%20%20%20%20%20%20%20%20state%0A%20%20%20%20%20%20%20%20url%0A%20%20%20%20%20%20%7D%0A%20%20%20%20%7D%0A%20%20%7D%0A%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "query ListHostEventsWithTickets($hostId: ID!) {\n  host(id: $hostId) {\n    id\n    name\n    eventsWithTickets {\n      nodes {\n        id\n        title\n        slug\n        state\n        url\n      }\n    }\n  }\n}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/universe/latest/actions/list-host-events-with-tickets?${params}`, {
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
| `query` | string | yes | Universe GraphQL query document to execute for this action. Default: `query ListHostEventsWithTickets($hostId: ID!) {\n  host(id: $hostId) {\n    id\n    name\n    eventsWithTickets {\n      nodes {\n        id\n        title\n        slug\n        state\n        url\n      }\n    }\n  }\n}`. |
| `variables` | object | no | Optional GraphQL variables object for the host events query. Default: `{"hostId":"69bc5b60b86a1d003cef1424"}`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Universe API returns.

## Native endpoint

Through the native Universe API, this operation is `POST /graphql` (base URL `https://www.universe.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-host-events-with-tickets.md) for the provider-specific parameters and requirements.

