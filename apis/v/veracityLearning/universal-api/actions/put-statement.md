# Veracity Learning: Put Statement

Creates a single statement in Veracity Learning using a statement ID.

```
POST https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/put-statement
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veracity Learning `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/put-statement" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "statementId": "string",
  "statement": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/put-statement', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "statementId": "string",
    "statement": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `statementId` | string | yes | Exact xAPI statement UUID to store. |
| `statement` | object | yes | xAPI Statement object to store. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Veracity Learning API returns.

## Native endpoint

Through the native Veracity Learning API, this operation is `PUT /statements` (base URL `https://sample-lrs-rafehwe.lrs.io/xapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/put-statement.md) for the provider-specific parameters and requirements.

