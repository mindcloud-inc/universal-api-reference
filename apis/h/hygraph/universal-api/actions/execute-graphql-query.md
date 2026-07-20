# Hygraph: Execute GraphQL Query

Executes a GraphQL query in Hygraph.

```
GET https://connect.mindcloud.co/v1/universal/hygraph/latest/actions/execute-graphql-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hygraph `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hygraph/latest/actions/execute-graphql-query?connectionId=$CONNECTION_ID&query=query%20%7B%20assets(first%3A%2010)%20%7B%20id%20fileName%20url%20%7D%20%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "query { assets(first: 10) { id fileName url } }"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hygraph/latest/actions/execute-graphql-query?${params}`, {
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
| `query` | string | yes | GraphQL query document to execute against the configured Hygraph Content API endpoint. Example: `query { assets(first: 10) { id fileName url } }`. |
| `variables` | object | no | Optional GraphQL variables object for the query. Example: `[object Object]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Hygraph API returns.

## Native endpoint

Through the native Hygraph API, this operation is `POST` (base URL `{{credentials.endpoint}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/execute-graphql-query.md) for the provider-specific parameters and requirements.

