# RECRU: Add Newsletter Unsubscribe



```
POST https://connect.mindcloud.co/v1/universal/rECRU/latest/actions/add-newsletter-unsubscribe
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RECRU `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rECRU/latest/actions/add-newsletter-unsubscribe" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rECRU/latest/actions/add-newsletter-unsubscribe', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RECRU API returns.

## Native endpoint

Through the native RECRU API, this operation is `POST` (base URL `https://mindclo.recru.eu/api/json-rpc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-newsletter-unsubscribe.md) for the provider-specific parameters and requirements.

