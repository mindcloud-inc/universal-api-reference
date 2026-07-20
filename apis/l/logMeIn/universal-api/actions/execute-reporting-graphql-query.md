# LogMeIn: Execute Reporting GraphQL Query

Executes a reporting GraphQL query in LogMeIn.

```
POST https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/execute-reporting-graphql-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LogMeIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/execute-reporting-graphql-query" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "query": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/execute-reporting-graphql-query', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "query": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | yes | GraphQL query string to execute against GoTo Resolve reporting. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables` | object | no | Optional GraphQL variables object. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native LogMeIn API returns.

## Native endpoint

Through the native LogMeIn API, this operation is `POST /goto-resolve-reporting/v1` (base URL `https://api.goto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/execute-reporting-graphql-query.md) for the provider-specific parameters and requirements.

