# Olvy: Query

Makes an authenticated raw API request to Olvy.

```
GET https://connect.mindcloud.co/v1/universal/olvy/latest/actions/query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Olvy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/olvy/latest/actions/query?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/olvy/latest/actions/query?${params}`, {
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
| `query` | string | yes | Raw GraphQL query document to execute against Olvy. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Olvy API returns.

## Native endpoint

Through the native Olvy API, this operation is `POST /` (base URL `https://app.olvy.co/api/v2/graphql`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query.md) for the provider-specific parameters and requirements.

