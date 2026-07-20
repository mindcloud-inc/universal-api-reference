# Fibery: GraphQL Query

Retrieves query results from Fibery GraphQL.

```
GET https://connect.mindcloud.co/v1/universal/fibery/latest/actions/graphql-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fibery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fibery/latest/actions/graphql-query?connectionId=$CONNECTION_ID&space=string&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "space": "string",
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fibery/latest/actions/graphql-query?${params}`, {
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
| `space` | string | yes | Fibery space name used in the GraphQL endpoint. |
| `query` | string | yes | GraphQL query text to execute. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fibery API returns.

## Native endpoint

Through the native Fibery API, this operation is `POST /graphql/space/:space` (base URL `https://{{credentials.account}}.fibery.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/graphql-query.md) for the provider-specific parameters and requirements.

