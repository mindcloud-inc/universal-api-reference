# Sourcegraph: Update Search Context

Updates a search context in Sourcegraph.

```
PUT https://connect.mindcloud.co/v1/universal/sourcegraph/latest/actions/update-search-context
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sourcegraph `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sourcegraph/latest/actions/update-search-context" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sourcegraph/latest/actions/update-search-context', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.description` | string | no | The updated search context description. |
| `variables.id` | string | no | The current Sourcegraph search context ID to update. If you rename a context, use the updated ID from the mutation response for future operations. |
| `variables.name` | string | no | The updated search context name. |
| `variables.query` | string | no | The updated repository filter query for the search context. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sourcegraph API returns.

## Native endpoint

Through the native Sourcegraph API, this operation is `POST /.api/graphql` (base URL `https://sourcegraph.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-search-context.md) for the provider-specific parameters and requirements.

