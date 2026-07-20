# RECRU: Echo Text



```
GET https://connect.mindcloud.co/v1/universal/rECRU/latest/actions/echo-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RECRU `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rECRU/latest/actions/echo-text?connectionId=$CONNECTION_ID&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rECRU/latest/actions/echo-text?${params}`, {
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
| `text` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RECRU API returns.

## Native endpoint

Through the native RECRU API, this operation is `POST` (base URL `https://mindclo.recru.eu/api/json-rpc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/echo-text.md) for the provider-specific parameters and requirements.

