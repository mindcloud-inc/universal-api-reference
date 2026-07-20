# Hygraph: Execute GraphQL Mutation

Executes a GraphQL mutation in Hygraph.

```
POST https://connect.mindcloud.co/v1/universal/hygraph/latest/actions/execute-graphql-mutation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hygraph `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hygraph/latest/actions/execute-graphql-mutation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "query": "mutation { publishAsset(where: { id: \"...\" }) { id } }"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hygraph/latest/actions/execute-graphql-mutation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "query": "mutation { publishAsset(where: { id: \"...\" }) { id } }"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | yes | GraphQL mutation document to execute against the configured Hygraph Content API endpoint. Example: `mutation { publishAsset(where: { id: "..." }) { id } }`. |
| `variables` | object | no | Optional GraphQL variables object for the mutation. Example: `[object Object]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Hygraph API returns.

## Native endpoint

Through the native Hygraph API, this operation is `POST` (base URL `{{credentials.endpoint}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/execute-graphql-mutation.md) for the provider-specific parameters and requirements.

