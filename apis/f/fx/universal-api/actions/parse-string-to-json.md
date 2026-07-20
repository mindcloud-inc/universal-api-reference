# 1001fx: Parse String to JSON

Parses a string into a JSON object.

```
POST https://connect.mindcloud.co/v1/universal/fx/latest/actions/parse-string-to-json
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1001fx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fx/latest/actions/parse-string-to-json" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "string": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fx/latest/actions/parse-string-to-json', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "string": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `string` | string | yes | String value to parse as JSON. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 1001fx API returns.

## Native endpoint

Through the native 1001fx API, this operation is `POST /data/parsestring2json` (base URL `https://api.1001fx.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/parse-string-to-json.md) for the provider-specific parameters and requirements.

