# Rasayel: GraphQL Query

Makes an authenticated raw GraphQL request to Rasayel.

```
GET https://connect.mindcloud.co/v1/universal/rasayel/latest/actions/graph-ql-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rasayel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rasayel/latest/actions/graph-ql-query?connectionId=$CONNECTION_ID&query=query%20GetApp%20%7B%20app%20%7B%20id%20displayName%20%7D%20%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "query GetApp { app { id displayName } }"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rasayel/latest/actions/graph-ql-query?${params}`, {
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
| `query` | string | yes | Enter a Rasayel GraphQL query. Example: `query GetApp { app { id displayName } }`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rasayel API returns.

## Native endpoint

Through the native Rasayel API, this operation is `POST /` (base URL `https://api.rasayel.io/api/graphql`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/graph-ql-query.md) for the provider-specific parameters and requirements.

