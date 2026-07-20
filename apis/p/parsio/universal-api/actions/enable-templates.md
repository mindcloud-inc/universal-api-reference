# Parsio: Enable Templates



```
PUT https://connect.mindcloud.co/v1/universal/parsio/latest/actions/enable-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Parsio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/parsio/latest/actions/enable-templates" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ids[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/parsio/latest/actions/enable-templates', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ids[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ids[]` | array<string> | yes | Template IDs to enable. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Parsio API returns.

## Native endpoint

Through the native Parsio API, this operation is `POST /templates/enable_many` (base URL `https://api.parsio.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enable-templates.md) for the provider-specific parameters and requirements.

