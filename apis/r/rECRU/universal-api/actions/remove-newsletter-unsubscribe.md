# RECRU: Remove Newsletter Unsubscribe



```
DELETE https://connect.mindcloud.co/v1/universal/rECRU/latest/actions/remove-newsletter-unsubscribe
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RECRU `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/rECRU/latest/actions/remove-newsletter-unsubscribe?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rECRU/latest/actions/remove-newsletter-unsubscribe?${params}`, {
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
| `email` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RECRU API returns.

## Native endpoint

Through the native RECRU API, this operation is `POST` (base URL `https://mindclo.recru.eu/api/json-rpc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-newsletter-unsubscribe.md) for the provider-specific parameters and requirements.

