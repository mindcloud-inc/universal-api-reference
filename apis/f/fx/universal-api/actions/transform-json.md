# 1001fx: Transform JSON

Transforms JSON into another structure using a template.

```
POST https://connect.mindcloud.co/v1/universal/fx/latest/actions/transform-json
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1001fx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fx/latest/actions/transform-json" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fx/latest/actions/transform-json', {
  method: 'POST',
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
| `inputJson` | object | no | Input JSON object to transform. |
| `inputJsonString` | string | no | Input JSON string to transform. |
| `templateJson` | object | no | Template JSON object that defines the output structure. |
| `templateJsonString` | string | no | Template JSON string that defines the output structure. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 1001fx API returns.

## Native endpoint

Through the native 1001fx API, this operation is `POST /data/json2json` (base URL `https://api.1001fx.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/transform-json.md) for the provider-specific parameters and requirements.

