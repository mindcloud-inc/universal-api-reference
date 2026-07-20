# NetExplorer: Send Upload Link SMS



```
POST https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-ulink-key-by-ulink-key-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-ulink-key-by-ulink-key-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ulinkKey": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-ulink-key-by-ulink-key-sms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ulinkKey": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ulinkKey` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native NetExplorer API returns.

## Native endpoint

Through the native NetExplorer API, this operation is `POST /ulink/key/:ulinkKey/sms` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ulink-key-by-ulink-key-sms.md) for the provider-specific parameters and requirements.

