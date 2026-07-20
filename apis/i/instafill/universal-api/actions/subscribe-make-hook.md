# Instafill: Subscribe Make Hook



```
POST https://connect.mindcloud.co/v1/universal/instafill/latest/actions/subscribe-make-hook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instafill `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instafill/latest/actions/subscribe-make-hook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instafill/latest/actions/subscribe-make-hook', {
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
| `hookurl` | string | no |  |
| `eventType` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Instafill API returns.

## Native endpoint

Through the native Instafill API, this operation is `POST /v1/integrations/make/hooks/subscribe` (base URL `https://api.instafill.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/subscribe-make-hook.md) for the provider-specific parameters and requirements.

