# Matterport: GraphQL Query

Makes an authenticated GraphQL request to Matterport.

```
GET https://connect.mindcloud.co/v1/universal/matterport/latest/actions/graph-ql-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Matterport `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/matterport/latest/actions/graph-ql-query?connectionId=$CONNECTION_ID&query=query%20%7B%20models%20%7B%20totalResults%20results%20%7B%20id%20name%20%7D%20%7D%20%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "query { models { totalResults results { id name } } }"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/matterport/latest/actions/graph-ql-query?${params}`, {
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
| `query` | string | yes | GraphQL query to send to Matterport. Example: `query { models { totalResults results { id name } } }`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables` | object | no | GraphQL variables object for the query. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Matterport API returns.

## Native endpoint

Through the native Matterport API, this operation is `POST api/models/graph` (base URL `https://api.matterport.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/graph-ql-query.md) for the provider-specific parameters and requirements.

