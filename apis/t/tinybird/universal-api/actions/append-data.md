# Tinybird: Append Data



```
POST https://connect.mindcloud.co/v1/universal/tinybird/latest/actions/append-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tinybird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tinybird/latest/actions/append-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tinybird/latest/actions/append-data', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `format` | string | no | Optional source format: csv, ndjson, or parquet |
| `name` | string | yes | Target data source name |
| `url` | string | yes | Remote file URL to append |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Tinybird API returns.

## Native endpoint

Through the native Tinybird API, this operation is `POST v0/datasources` (base URL `{{credentials.apiHost}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/append-data.md) for the provider-specific parameters and requirements.

