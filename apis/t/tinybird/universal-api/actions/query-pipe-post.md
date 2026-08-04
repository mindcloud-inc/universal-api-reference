# Tinybird: Query Pipe (POST)



```
GET https://connect.mindcloud.co/v1/universal/tinybird/latest/actions/query-pipe-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tinybird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tinybird/latest/actions/query-pipe-post?connectionId=$CONNECTION_ID&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tinybird/latest/actions/query-pipe-post?${params}`, {
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
| `name` | string | yes | The published Pipe name. |
| `q` | string | no | Optional query parameters for the Pipe. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Tinybird API returns.

## Native endpoint

Through the native Tinybird API, this operation is `POST v0/pipes/:name.json` (base URL `{{credentials.apiHost}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-pipe-post.md) for the provider-specific parameters and requirements.

